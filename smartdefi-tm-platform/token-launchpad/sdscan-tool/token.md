# 🔶 Token

Usar para administrar el token SmartDeFi. Accesible a través de SDscan - Token - Contrato de token

<mark style="color:orange;">**Esta página está en desarrollo**</mark>

### **Leer**

<details>

<summary>Comandos de lectura</summary>

1. BackingLogicAddress() - verifica el contrato de activo de respaldo del token
2. DATA\_READ()
3. LGE()
4. LGEAddress()
5. LGELive()
6. LPBURN()
7. UNISWAP\_V2\_ROUTER()
8. User(address)
9. WETH()
10. \_UNISWAP\_V2\_ROUTER()
11. allFee(uint256) - es necesario llamar a cada uno por separado. 0-5 Impuestos de compra/transferencia, 6-11 Impuestos de venta

    respaldo: 0,

    &#x20; quema: 1,

    &#x20; liquidez: 2,

    &#x20; crecimiento: 3,

    &#x20; staking: 4,

    &#x20; reflexión: 5,

    respaldo: 6,

    &#x20; quema: 7,

    &#x20; liquidez: 8,

    &#x20; crecimiento: 9,

    &#x20; staking: 10,

    &#x20; reflexión: 11


12. allLastBalance(address)
13. allUser(uint256)
14. allowance(address,address) - verifica si se ha otorgado aprobación para el gasto (por ejemplo, para verificar si el token fue aprobado para ser usado por contratos inteligentes adicionales).
15. backingThreshold() - Umbral para que el contrato de respaldo convierta tokens en activos de respaldo acumulados del impuesto de respaldo&#x20;
16. balance(address,uint256)
17. balanceOf(address) - verifica el saldo de la billetera o contrato
18. blockNumber(address,uint256)
19. checkLiquidityLock(address) - Verifica si la liquidez está bloqueada en el contrato del token SD&#x20;
20. checkWhiteListContract(address) - Verifica si un contrato está en la lista blanca
21. decimals() - Comprueba cuántos decimales tiene un token
22. frontRun(address,uint256)
23. getAllFee(uint256)
24. isExchange(address) - verifica si el contrato está asignado con el estado de Exchange (aplica impuestos tokenomics)
25. lastBalance(address)
26. liqShare()
27. liquidityThreshold() - Umbral para que el contrato de liquidez convierta tokens acumulados del impuesto de Liquidez en el activo emparejado (si el token está emparejado con WBNB, el contrato convertirá los tokens acumulados en WBNB).
28. liquidityUnlockTime(address) - Verifica el tiempo para el desbloqueo de liquidez si se bloquearon tokens LP en el SD Lock. No se refiere al servicio de lockers de tokens de terceros.
29. name() - nombre del token
30. onlySB()
31. owner() - propietario de SD
32. sdFeeRecipient()
33. sdOwner() - Verifica el propietario del token SD
34. sdStake()
35. suggestedAllFee(uint256)
36. suggestedOnlySB()
37. symbol() - obtiene el símbolo del token
38. taxFree(address) - comprueba la dirección de la billetera o del contrato si está libre de impuestos
39. timeDelay()
40. tokenFromGift(uint256)
41. totalHolders() - obtiene el número total de titulares
42. totalSupply() - obtiene la oferta total
43. uniswapV2Pair()

</details>

\
**Escribir**

<details>

<summary>Comandos de escritura</summary>

Los comandos de escritura permiten la comunicación directa con los contratos inteligentes del token SmartDeFi. Algunas funciones están disponibles solo para propietarios y otras funciones están disponibles para cualquiera.&#x20;

1. afterConstructor()
2.  approve(address,uint256) - Si deseas permitir que la billetera X mueva Y cantidad de tokens SD

    gastador (address) - ingresa la dirección de la billetera/contrato al que deseas dar aprobación

    cantidad (uint256) - ingresa la cantidad deseada + 18 ceros


3. endLGE()
4.  extendLiquidityLock(uint256,address) - Después de bloquear tus LP en el contrato del token, puedes usar esta función para extender el tiempo de bloqueo el tiempo que desees.

    díasBloqueo (uint256) - ingresa “1” si deseas extender por 1 día. Sin decimales

    dirección (address) - ingresa la dirección LP de tu token

    Mín: 1 día

    Máx: 9 seguido de 70 nueves

    Quién puede acceder: Propietario del proyecto\

5.  initialLockLiquidity(uint256,address,uint256) - Cuando desees bloquear tus tokens LP directamente dentro del contrato del token SD, deberás usar esta función.

    Para poder usar esta función, la primera vez que la uses necesitarás hacer una aprobación adicional.

    Ejemplo para el lado de BNB: Ve al contrato LP en BSCscan en WRITE y en "1. Approve" ingresa esto:

    gastador (address)  -  ingresa la dirección del contrato de tu token

    valor (uint256) -- pon un número masivo como 1000000000000000000000000000000000000000000000000000000000000000000

    Ve a READ en el contrato de LP y obtén "balance of" de tu billetera y copia ese número.

    Ahora regresa a FEGscan en WRITE y en “5. initialLockLiquidity” ingresa así:

    díasBloqueo (uint256) - ingresa “1” para bloquear por 1 día. Sin decimales.

    dirección (address) - ingresa la dirección LP de tu token

    cant (uint256) - ingresa la cantidad de tokens LP que desees bloquear + 18 ceros o simplemente pega el número que copiaste antes de “balance of” en BSCscan

    Mín: 1 día

    Máx: 2.74 trevigintillion años (9 seguido de 71 nueves)

    Acceso: Propietario del proyecto


6.  manualBurn(uint256,uint256,uint256) - será descontinuado


7.  removeLiquidity(uint256,address) - Usa esta función para recuperar tus tokens LP desde dentro del contrato del token SD DESPUÉS de que expire el tiempo de bloqueo.

    También puedes usar esta función para recuperar CUALQUIER token, en cualquier momento, enviado al contrato del token por otras personas por error.

    cant (uint256) - ingresa la cantidad de tokens que deseas recuperar + 18 ceros

    dirección (address) - ingresa la dirección de los tokens LP, o la dirección del contrato de los tokens que deseas eliminar si alguien envió varios tokens por error directamente al contrato del token.

    Acceso: Propietario del proyecto


8.  setBackingThreshold(uint256) - El contrato de respaldo acumula tokens SD dentro del impuesto de respaldo y luego, cuando se alcanza el límite de la cantidad de tokens almacenados, vende dichos tokens SD en el mercado a cambio de los tokens de respaldo que elegiste para tu proyecto. Por ejemplo, vende FEG por wBNB.

    Por defecto, el límite se establece en 0.01% de la oferta total.&#x20;

    cant (uint256) - ingresa el número de tokens + 18 ceros

    Acceso: Propietario del proyecto


9.  setExchange(address,bool) - Si creas un nuevo par de pool de intercambio en otra plataforma para tu proyecto SD, puedes usar esta función para habilitar que los impuestos de trading funcionen correctamente para ese nuevo pool de liquidez.&#x20;

    LP (address) - ingresa la dirección del pool de liquidez para el que deseas habilitar los impuestos de trading

    agregando (bool) - ingresa TRUE para habilitar los impuestos de trading&#x20;

    Acceso: Propietario del proyecto


10. setFee() - Una vez que se alcanza el límite de tiempo después de que el propietario del proyecto SD sugiere un nuevo porcentaje de impuestos, cualquier usuario puede usar esta función para activar los nuevos porcentajes de impuestos para el trading. Si no se utiliza esta función, el trading continuará con los impuestos antiguos.

    Acceso: cualquiera


11. setLGE(address)
12. setLiquidityThreshold(uint256) - El contrato de respaldo acumula tokens SD dentro del impuesto LP y luego, cuando se alcanza el límite de la cantidad de tokens almacenados, vende dichos tokens SD en el mercado a cambio de wBNB, que enviará/inyectará en el pool de liquidez, afectando así la relación token-a-WBNB y aumentando el precio de los tokens.

    Por defecto, el límite se establece en 0.01% de la oferta total.&#x20;

    cant (uint256) - ingresa la cantidad deseada de tokens para el límite + 18 ceros

    Acceso: Propietario del proyecto


13. setNewOwner(address) - Cuando desees cambiar el propietario del proyecto, usarás esta función e ingresarás la dirección de la billetera que deseas sea el nuevo propietario. También puedes ren