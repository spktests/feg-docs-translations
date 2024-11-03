# 🔶 Token

Usado para gestionar el token SmartDeFi. Accesible a través de SDscan - Token - Contrato de Token

<mark style="color:orange;">**Esta página está en desarrollo**</mark>

### **Leer**

<details>

<summary>Comandos de lectura</summary>

1. BackingLogicAddress() - verificar el contrato de activos de respaldo del token
2. DATA\_READ()
3. LGE()
4. LGEAddress()
5. LGELive()
6. LPBURN()
7. UNISWAP\_V2\_ROUTER()
8. User(address)
9. WETH()
10. \_UNISWAP\_V2\_ROUTER()
11. allFee(uint256) - necesita llamarse cada uno por separado. 0-5 Impuesto de Compra/Transferencia, 6-11 Impuesto de Venta

    backing: 0,

    &#x20; burn: 1,

    &#x20; liquidity: 2,

    &#x20; growth: 3,

    &#x20; staking: 4,

    &#x20; reflection: 5,

    backing: 6,

    &#x20; burn: 7,

    &#x20; liquidity: 8,

    &#x20; growth: 9,

    &#x20; staking: 10,

    &#x20; reflection: 11

12. allLastBalance(address)
13. allUser(uint256)
14. allowance(address,address) - verificar si se ha otorgado la asignación para el gasto (por ejemplo, para comprobar si se aprobó el uso del token por contratos inteligentes adicionales).
15. backingThreshold() - Umbral para que el Contrato de Respaldo convierta tokens en respaldo de activos que se acumularon del Impuesto de Respaldo.
16. balance(address,uint256)
17. balanceOf(address) - verificar el saldo de la billetera o contrato
18. blockNumber(address,uint256)
19. checkLiquidityLock(address) - verificar si una liquidez está bloqueada en el contrato del token SD
20. checkWhiteListContract(address) - verificar si un contrato está en la lista blanca
21. decimals() - verificar cuántos decimales tiene un token
22. frontRun(address,uint256)
23. getAllFee(uint256)
24. isExchange(address) - verificar si el contrato tiene asignado el estado de Intercambio (se aplican impuestos de tokenómica)
25. lastBalance(address)
26. liqShare()
27. liquidityThreshold() - Umbral para que el contrato de liquidez convierta tokens acumulados del impuesto de Liquidez al activo emparejado (si el token está emparejado con WBNB, el contrato convertirá tokens acumulados a WBNB).
28. liquidityUnlockTime(address) - Verificar el tiempo para el desbloqueo de liquidez si los tokens LP fueron bloqueados en el Bloqueo SD. No se refiere a los proveedores de servicios de bloqueo de tokens de terceros.
29. name() - nombre del token
30. onlySB()
31. owner() - propietario de SD
32. sdFeeRecipient()
33. sdOwner() - verificar el propietario del token SD
34. sdStake()
35. suggestedAllFee(uint256)
36. suggestedOnlySB()
37. symbol() - obtener el símbolo del token
38. taxFree(address) - verificar si una dirección de billetera o contrato está exenta de impuestos
39. timeDelay()
40. tokenFromGift(uint256)
41. totalHolders() - obtener número de titulares total
42. totalSupply() - obtener suministro total
43. uniswapV2Pair()

</details>

\
**Escribir**

<details>

<summary>Comandos de escritura</summary>

Los comandos de escritura permiten la comunicación directa con los contratos inteligentes del token SmartDeFi. Algunas funciones están disponibles solo para propietarios y otras funciones están disponibles para cualquiera.&#x20;

1. afterConstructor()
2. approve(address,uint256) - Si deseas permitir que la billetera X mueva una cantidad Y de tokens SD

    spender (address) - ingresa la dirección de la billetera/contrato al que deseas dar aprobación

    amount (uint256) - ingresa la cantidad deseada + 18 ceros

3. endLGE()
4. extendLiquidityLock(uint256,address) - Después de bloquear tu LP en el contrato del token, puedes usar esta función para extender el tiempo de bloqueo el tiempo que quieras.

    lockDays (uint256) - ingresa “1” si deseas extender por 1 día. Sin decimales

    address (address) - ingresa la dirección LP de tu token

    Mín: 1 días

    Máx: 9 seguido por 70 nueves

    Quién puede acceder: Propietario del proyecto\

5. initialLockLiquidity(uint256,address,uint256) - Cuando deseas bloquear tus tokens LP directamente dentro del contrato del token SD, deberás usar esta función.

    Para poder usar esta función, la primera vez que la utilices, necesitarás una aprobación adicional.

    Ejemplo para el lado BNB: Ve al contrato LP en BSCscan en WRITE y en “1. Approve” ingresa esto:

    spender (address)  -  ingresa la dirección del contrato de tu token

    value (uint256) -- pon un número masivo como 1000000000000000000000000000000000000000000000000000000000000000000

    Ve a READ en el contrato LP y obtén "balance of" de tu billetera y copia ese número.

    Ahora vuelve a FEGscan en WRITE y en “5. initialLockLiquidity” ingresa así:

    lockDays (uint256) - ingresa “1” para bloquear por 1 día. Sin decimales.

    address (address) - ingresa la dirección LP de tu token

    amt (uint256) - ingresa la cantidad de tokens LP que deseas bloquear + 18 ceros o simplemente pega el número que copiaste antes de “balance of” en BSCscan

    Mín: 1 días

    Máx: 2.74 años trevigintillion (9 seguido por 71 nueves)

    Acceso: Propietario del proyecto

6. manualBurn(uint256,uint256,uint256) - será descontinuado

7. removeLiquidity(uint256,address) - Usa esta función para recuperar tus tokens LP del interior del contrato del token SD DESPUÉS de que expire el tiempo de bloqueo.

    También puedes usar esta función para recuperar CUALQUIER token, en cualquier momento, enviado por error por otras personas al contrato del token.

    amt (uint256) - ingresa la cantidad de tokens que deseas recuperar + 18 ceros

    address (address) - ingresa la dirección de los tokens LP, o la dirección del contrato de los tokens que deseas eliminar si alguien envió varios tokens por error directamente al contrato del token.

    Acceso: Propietario del proyecto

8. setBackingThreshold(uint256) - El contrato de respaldo acumula tokens SD dentro del impuesto de respaldo y luego, cuando el límite de cantidad de tokens almacenado se alcanza, vende dichos tokens SD en el mercado a cambio de cualquier token de respaldo que hayas seleccionado para tu proyecto. Por ejemplo, vende FEG por wBNB.

    Por defecto el límite está establecido en 0.01% del suministro total.&#x20;

    amt (uint256) - ingresa el número de tokens + 18 ceros

    Acceso: Propietario del proyecto

9. setExchange(address,bool) - Si creas un nuevo par de trading en otro intercambio para tu proyecto SD, puedes usar esta función para habilitar que los impuestos de trading funcionen correctamente para ese nuevo pool de liquidez.&#x20;

    LP (address) - ingresa la dirección del pool de liquidez para el cual deseas habilitar los impuestos de trading

    adding (bool) - ingresa TRUE para habilitar los impuestos de trading&#x20;

    Acceso: Propietario del proyecto

10. setFee() - Una vez se alcanza el límite de tiempo después de que el propietario del proyecto SD sugiere un nuevo porcentaje de impuestos, cualquier usuario puede usar esta función para activar los nuevos porcentajes de impuestos para el trading. Si esta función no se utiliza, el trading continuará con los impuestos antiguos.

    Acceso: cualquier persona

11. setLGE(address)
12. setLiquidityThreshold(uint256) - El contrato de respaldo acumula tokens SD dentro del impuesto de LP y luego, cuando el límite de cantidad de tokens almacenado se alcanza, vende dichos tokens SD en el mercado a cambio de wBNB, que enviará/inyectará en el pool de liquidez, afectando así la relación token-to-wBNB y aumentando el precio de los tokens.

    Por defecto el límite está establecido en 0.01% del suministro total.&#x20;

    amt (uint256) - ingresa la cantidad deseada de tokens para el límite + 18 ceros

    Acceso: Propietario del proyecto

13. setNewOwner(address) - Cuando deseas cambiar el propietario del proyecto, usarás esta función e ingresarás la dirección de la billetera que deseas que sea el nuevo propietario. También puedes renunciar a la propiedad del proyecto ingresando la dirección de la billetera DEAD (la que tiene muchos ceros).

    newOwner