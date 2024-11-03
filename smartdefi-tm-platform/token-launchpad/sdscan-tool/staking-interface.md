# 🟡 Staking - Interfaz

<mark style="color:orange;">**Esta página está en desarrollo**</mark>

**Disponible a través de SDscan - Staking - Interfaz (después de que el Protocolo de Staking sea lanzado).**

<details>

<summary>Leer</summary>

1. DATA\_READ()
2. SD()
3. \_owner()
4. amountStaked(address)
5. balanceOf(address)
6. boost()
7. boostBacking()
8. burnWDFee()
9. decimals()
10. delay()
11. depositFee()
12. getAllPendingRewardTokenEarned(address)
13. getPaginatedPendingRewardTokenEarned(address,uint256,uint256)
14. getRewardList()
15. getRewardRound(address)
16. getRewardRounds(address,uint256)
17. getRewards(address)
18. getStakeTime(address)
19. getStakers(address)
20. getSyncLevel(address)
21. getTotalRewards(address)
22. getUserRewards(address,address)
23. isLive()
24. isStaker(address)
25. matureDelay()
26. name()
27. ownad()
28. owner()
29. paused()
30. pendingRewardTokenEarned(address,address)
31. rewardAddresses(uint256)
32. rewardLength()
33. sacrificeEnabled()
34. stakeDeployerAddress()
35. stakeLogic()
36. symbol()
37. totalStakedSD()
38. totalSupply()
39. userRewardCheck(address)
40. withdrawalFee()

</details>

<details>

<summary>Escribir</summary>

1.  addReward(address,uint256) - Addreward se utiliza para enviar recompensas (ejemplo wBNB) a los usuarios como pago.

    Hay 2 formas de usar addReward.&#x20;

    Usa addReward. Esto actualiza la ronda y distribuye.

    Introduce el contrato de token de recompensa e introduce la cantidad +18 ceros.

    Alternativamente, puedes enviar la recompensa al contrato vía transferencia. Esto usará el nivel de sincronización para determinar cuándo auto distribuir. Si el nivel de sincronización es de 10 tokens, una vez que haya más de 10 tokens se distribuirá en el próximo evento que tenga sincronización adjunta. (Como reclamar recompensa)


2.  claimAllReward() - Reclamar recompensas - Reclama todas las recompensas acumuladas.&#x20;

    Nota que hay una división obligatoria de 30 días para recompensas (lo que significa que obtienes el 50% de las recompensas si reclamas o desbloqueas en los primeros 30 días, después de 30 días manteniéndote en staking y no reclamando obtienes la otra mitad de las recompensas. En otras palabras: Si reclamaste la mitad perdiste la otra mitad (se dio a otros). Si esperas hasta después de 30 días para reclamar puedes reclamar todo.
3. claimRewardTokenEarned(address) - reclamar recompensa específica (se aplican reglas de 30 días)
4. emergencySaveLostTokens(address,address,uint256)
5. renounceOwnership() - renunciar a la propiedad de los derechos de gestión del protocolo de staking (esto eliminará los derechos de gestión para el protocolo de staking). Introduce la dirección del monedero burn y confirma la transacción.
6. sendReward(address,address,uint256)
7. sendTokens(address,uint256)
8. setBoost(uint256) - introduce 10 para 1%, 1 para 0.1% etc. El máximo es 100% (1000 y menos)
9.  setBoostBacking(bool) - Si tu SD tiene respaldo (por ejemplo, en wbnb) y tu recompensa es la misma (wbnb). Boost backing tomará un % de addReward y enviará al respaldo. Aplicable sólo a propietarios de SD.

    Introduce true para sí boost y false para no boost


10. setBurnWDFee(bool) - BurnWD quemará la tarifa de depósito o retirada (si las tarifas están establecidas) si burnWDfee está apagado y la tarifa de depósito o retirada está encendida se distribuirán las recompensas a los stakeholders.

    Introduce&#x20;

    true - si quieres que las tarifas de retirada y depósito se envíen a quemar

    false - si quieres redistribuir las tarifas de retirada/deposito a los stakeholders


11. setDelay(uint256) - El retraso es la cantidad de demora si matureDelay es verdadero

    Formato de entrada:

    1 para 1 día

    Mínimo 1 día, máximo es 30 días.

    Los stakeholders antiguos después de 30 días pueden retirarse incluso si el propietario del proyecto reinicia el contador de 30 días, el retraso maduro se aplicará a los nuevos stakeholders.

    Si alguien hace staking en el día 29 podrá desbloquear en 1 día porque el bloqueo termina para ese período.&#x20;


12. setDepositFee(uint256) - Establecer tarifa para staking

    Introduce 10 para el formato de 1%

    Máximo es 20%\

13. setLogics(address)
14. setMatureDelay(bool) - MatureDelay es cuando puedes salir de un stake. Es opcional y difiere de la división de 30 días.

    El retraso establecerá el bloqueo de desbloqueo, por lo que se puede decir: hacer staking por X cantidad de días y no se puede salir. Si no estableces un retraso, los stakeholders pueden salir en cualquier momento pero todavía están bajo la regla de división de recompensas de 30 días.

    matureDelay es el bool que se establece si deseas imponer un retraso.

    Introduce

    true - si quieres imponer un plazo específico para cuanto tiempo los stakeholders no podrán dejar de hacer staking

    false - si no quieres imponer esto\

15. setRewardToken(address,uint256)- Usa esto para establecer tokens de recompensa y un umbral (nivel de sincronización).&#x20;

    SetReward añade un nuevo token de recompensa como agregar wbtc.

    Introduce el contrato del token de recompensa

    Introduce el nivel de sincronización +18 ceros (1+18 ceros=1)

    Incluso si elegiste wbnb durante el despliegue (por ejemplo), todavía necesitas establecer el umbral en el que ocurrirá la distribución. Puedes usar cualquier erc20/bep20 (o contratos de testnet, tokens lp y tokens SD). SetReward no es aplicable al token SD nativo (por ejemplo, no necesitas setReward para el propio token SD, sólo para los tokens de recompensa adicionales (busd, dai, wbnb etc).

    Ejemplo, si quieres que las recompensas de staking en wbnb se distribuyan con cada 0.5 wbnb añadido al contrato de staking:

    Introduce el contrato del token de recompensa

    0xae13d989daC2f0dEbFf460aC112a837C89BAa7cd

    Introduce el nivel de sincronización +17 ceros

    500000000000000000

    Aprueba transacciones.&#x20;

    El nivel de sincronización mínimo es 1e7 (1+7 ceros = 10000001 lo que es equivalente a 0.0000001 de un token). \

16. setSacrificeEnabled(bool) - Establece True o False para activarlo en el lado del propietario y permitir a los usuarios elegir si desean quemar sus recompensas mediante la función Sacrifice

    _Acceso: Propietarios del Proyecto_\

17. setSacrificeLevel(uint256) - Sólo los stakers pueden usar esto: pueden elegir % de las recompensas que quieren enviar a quemar en su lugar.

    Introduce 100 para 10%, 10 para 1%, 1 para 0.1%. El máximo es 600 (60%), el mínimo es 0. Set Sacrifice debe ser habilitado por el propietario del proyecto primero antes de que los stakers puedan elegir el %

    _Acceso: Stakers_\

18. setStakeLogic()
19. setSyncLevel(address,uint256) - setSyncLevel cambia el nivel de sincronización guardado de la recompensa (el nivel que se pagará automáticamente)

    Introduce la dirección del token de recompensa y la cantidad en un formato 1+18 ceros&#x20;


20. setWithdrawalFee(uint256) - Establecer tarifa por dejar de hacer staking

    Introduce 10 para el formato de 1%

    Máximo 20%


21. stake(uint256) - Introduce la cantidad de tokens que quieres hacer staking

    1+18 ceros por 1 token


22. start() - Activa tu staking para que los inversores puedan comenzar a hacer staking
23. syncRewards()
24. transferOwnership(address) - puedes transferir los derechos de gestión de tu staking a otro monedero. Introduce la dirección y confirma la transacción. Después, el propietario del token no tendrá acceso a la gestión del staking si el monedero elegido para la transferencia de propiedad será controlado por otra persona/entidad/DAO.
25. withdraw(uint256) - Introduce la cantidad a desbloquear&#x20;

    1+18 ceros por 1 token

    \


</details>