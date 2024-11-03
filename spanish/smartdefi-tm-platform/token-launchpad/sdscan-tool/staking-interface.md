# 🟡 Staking - Interfaz

<mark style="color:orange;">**Esta página está en desarrollo**</mark>

**Disponible a través de SDscan - Staking - Interfaz (después del lanzamiento del Protocolo de Staking).**

<details>

<summary>Leer</summary>

1. DATA\_READ()
2. SD()
3. \_owner()
4. amountStaked(dirección)
5. balanceOf(dirección)
6. boost()
7. boostBacking()
8. burnWDFee()
9. decimals()
10. delay()
11. depositFee()
12. getAllPendingRewardTokenEarned(dirección)
13. getPaginatedPendingRewardTokenEarned(dirección,uint256,uint256)
14. getRewardList()
15. getRewardRound(dirección)
16. getRewardRounds(dirección,uint256)
17. getRewards(dirección)
18. getStakeTime(dirección)
19. getStakers(dirección)
20. getSyncLevel(dirección)
21. getTotalRewards(dirección)
22. getUserRewards(dirección,dirección)
23. isLive()
24. isStaker(dirección)
25. matureDelay()
26. name()
27. ownad()
28. owner()
29. paused()
30. pendingRewardTokenEarned(dirección,dirección)
31. rewardAddresses(uint256)
32. rewardLength()
33. sacrificeEnabled()
34. stakeDeployerAddress()
35. stakeLogic()
36. symbol()
37. totalStakedSD()
38. totalSupply()
39. userRewardCheck(dirección)
40. withdrawalFee()

</details>

<details>

<summary>Escribir</summary>

1.  addReward(dirección,uint256) - Addreward es para enviar recompensas (por ejemplo wBNB) a los usuarios como un pago.

    Hay 2 formas de addReward.&#x20;

    Use addReward. Esto actualiza la ronda y distribuye

    Ingrese el contrato de token de recompensa y la cantidad +18 ceros

    Alternativamente, puede enviar la recompensa al contrato mediante transferencia. Esto usará synclevel para determinar cuándo distribuir automáticamente. Si synclevel es 10 tokens, una vez haya más de 10 tokens se distribuirá en el siguiente evento que tenga sincronización adjunta. (Como reclamar recompensa)

2.  claimAllReward() - Reclamar recompensas - Reclama todas las recompensas acumuladas.&#x20;

    Tenga en cuenta que existe una división obligatoria de 30 días para las recompensas (lo que significa que obtiene el 50% de las recompensas si reclama o retira dentro de los primeros 30 días, después de 30 días permaneciendo en staking y sin reclamar, obtiene la otra mitad de las recompensas. En otras palabras: Si reclamó la mitad, perdió la otra mitad (se la dio a otros). Si espera hasta después de 30 días para reclamar, puede reclamar todo.
3. claimRewardTokenEarned(dirección) - reclamar recompensa específica (reglas de 30 días aplicables)
4. emergencySaveLostTokens(dirección,dirección,uint256)
5. renounceOwnership() - renunciar a los derechos de gestión del protocolo de staking (esto eliminará los derechos de gestión del protocolo de staking). Ingrese la dirección de la billetera quemada y confirme la transacción.
6. sendReward(dirección,dirección,uint256)
7. sendTokens(dirección,uint256)
8. setBoost(uint256) - ingrese 10 para 1%, 1 para 0.1%, etc. El máximo es 100% (1000 y por debajo)
9.  setBoostBacking(bool) - Si su SD tiene respaldo (por ejemplo, en wbnb) y su recompensa es la misma (wbnb). Boost backing tomará un % de addReward y enviará al respaldo. Aplicable solo a los dueños de SD.

    Ingrese verdadero para sí aumentar y falso para no aumentar

10. setBurnWDFee(bool) - BurnWD quemará la tarifa de depósito o retiro (si las tarifas están configuradas) si burnWDfee está apagado y la tarifa de depósito o retiro está encendida, distribuirá recompensas a los stakers.

    Ingrese&#x20;

    true - si desea que las tarifas de retiro y depósito se envíen a quemar

    false - si desea redistribuir las tarifas de retiro/deposito a los stakers

11. setDelay(uint256) - El retraso es la cantidad de retraso si matureDelay es verdadero

    Formato de entrada:

    1 por 1 día

    Mínimo 1 día, máximo es 30 días.

    Los stakers más antiguos después de 30 días pueden salir incluso si el propietario del proyecto reinicia el contador de 30 días, el retraso maduro se aplicará a los nuevos stakers.

    Si alguien apuesta el día 29 podrá retirarse en 1 día porque el bloqueo termina para ese período.&#x20;

12. setDepositFee(uint256) - Establecer tarifa para staking

    Entrada 10 para formato 1%

    El máximo es del 20%\

13. setLogics(dirección)
14. setMatureDelay(bool) - MatureDelay es cuando puedes salir de un stake. Es opcional y se diferencia de los 30 días de división de recompensas.

    El retraso establecerá el bloqueo de desestaking, por lo que puede decir: apuesta por X días y no puedes irte. Si no configura un retraso, los stakers pueden irse en cualquier momento, pero aún están bajo la regla de división de recompensas de 30 días.

    matureDelay es el bool que se establece si deseas imponer un retraso.

    Entrada

    true - si desea imponer un plazo específico para cuánto tiempo los stakers no podrán retirar

    false - si no quieres imponer esto\

15. setRewardToken(dirección,uint256)- Usa esto para establecer tokens de recompensa y un umbral (nivel de sincronización).&#x20;

    SetReward añade un nuevo token de recompensa como agregar wbtc.

    Ingrese el contrato de token de recompensa

    Introduzca el nivel de sincronización +18 ceros (1+18 ceros=1)

    Incluso si eligió wbnb durante la implementación (por ejemplo), aún necesita establecer el umbral en el que se realizará la distribución. Puede usar cualquier erc20/bep20 (o contratos de testnet, tokens lp y tokens SD). SetReward no es aplicable al token SD nativo (por ejemplo, no necesita setRward para el propio token SD, solo para los tokens de recompensa adicionales (busd, dai, wbnb, etc).

    Ejemplo, si desea que las recompensas por staking en wbnb se distribuyan con cada 0.5 wbnb agregado al contrato de staking:

    Introduzca el contrato de token de recompensa

    0xae13d989daC2f0dEbFf460aC112a837C89BAa7cd

    Introduzca el nivel de sincronización +17 ceros

    500000000000000000

    Aprobar transacciones.&#x20;

    El nivel mínimo de sincronización es 1e7 (1+7 ceros = 10000001, lo que equivale a 0.0000001 de un token). \

16. setSacrificeEnabled(bool) - Establezca True o False para activarlo del lado del propietario para permitir a los usuarios elegir si desean quemar sus recompensas mediante la función de Sacrificio

    _Acceso: Propietarios del Proyecto_\

17. setSacrificeLevel(uint256) - Solo los stakers pueden usar esto: pueden elegir el % de las recompensas que desean enviar a quemar en su lugar.

    Entrada 100 para 10%, 10 para 1%, 1 para 0.1%. El máximo es 600 (60%), el mínimo es 0. El Sacrificio debe estar habilitado por el propietario del proyecto antes de que los stakers puedan elegir el %

    _Acceso: Stakers_\

18. setStakeLogic()
19. setSyncLevel(dirección,uint256) - setSyncLevel cambia el nivel de sincronización guardado de la recompensa (el nivel en el que se pagará automáticamente)

    Ingrese la dirección del token de recompensa y la cantidad en un formato 1+18 ceros&#x20;

20. setWithdrawalFee(uint256) - Establecer tarifa para desestaking

    Entrada 10 para formato 1%

    Máximo 20%

21. stake(uint256) - Ingrese la cantidad de tokens que desea apostar

    1+18 ceros para 1 token

22. start() - Activa tu staking para que los inversores puedan comenzar a hacer staking
23. syncRewards()
24. transferOwnership(dirección) - puede transferir derechos de gestión para su staking a otra billetera. Ingrese la dirección y confirme la transacción. Después, el dueño del token no tendrá acceso a la gestión de Staking si una billetera elegida para la transferencia de propiedad será controlada por otra persona/entidad/DAO.
25. withdraw(uint256) - Ingrese la cantidad para retirar&#x20;

    1+18 ceros para 1 token

    \

</details>