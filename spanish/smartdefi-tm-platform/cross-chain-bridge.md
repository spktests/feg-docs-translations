# ⛓️ Puente Cross-chain

<figure><img src="../.gitbook/assets/Screenshot_14 (1).png" alt=""><figcaption></figcaption></figure>

Presentamos el Puente Cross-Chain On-Chain de SmartDeFi, una característica revolucionaria disponible para todos los proyectos lanzados desde el SmartDeFi Token Launchpad.

El Puente abre un mundo de posibilidades con interoperabilidad sin fisuras entre diferentes blockchains EVM, completamente en la cadena, donde los usuarios ahora pueden disfrutar de una flexibilidad, arbitraje y accesibilidad inigualables al gestionar sus tokens.

Únete a nosotros en este emocionante viaje hacia un ecosistema más interconectado y descentralizado.

### Cómo Funciona

<figure><img src="../.gitbook/assets/bridge 1 FEG base to bnb.jpg" alt=""><figcaption></figcaption></figure>

Dirígete a [SmartDeFi.com](https://smartdefi.com), conecta tu billetera, elige el token que deseas puentear y luego haz clic en la pestaña "Bridge".

En este punto se te dará la oportunidad de elegir a qué cadena deseas puentear, el siguiente paso es que necesitas ingresar la cantidad de tokens para puentear de la cadena X a la cadena Y. Por último, deberás hacer clic en el botón "Aprobar" y luego en el botón "Bridge" para realizar la transacción de puente real.

Ahora, lo único que queda por hacer es cambiar la red de tu billetera a la cadena a la que enviaste los tokens, luego asegúrate de estar en la pestaña "Bridge" y en la pestaña "Retiros". Verifica que toda la información mostrada sea correcta y luego haz clic en el botón "Retirar".

{% hint style="success" %}
Recuerda que necesitas monedas nativas para las tarifas de gas tanto en las cadenas de origen como de destino.

¡Las tarifas de gas para el uso del puente son más altas que las transacciones normales!
{% endhint %}

Y eso es todo, has puenteado tus tokens a otra cadena en unos pocos clics, simple y fácil.

<figure><img src="../.gitbook/assets/withdraw bridge 1FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
El puente está limitado a una instancia de puenteo cada 15 minutos.

El usuario tiene hasta 30 días para reclamar activos del SmartBridge.

Los activos no reclamados se perderán para siempre.
{% endhint %}

### FAQ

1. **¿Quién Puede Iniciar la Creación del Puente?**
   * Solo el propietario del contrato inteligente del token de SmartDeFi puede iniciar la creación del puente. Esto asegura acceso autorizado y verificación de la billetera del propietario a través de las cadenas.
2. **¿Puede Distribuirse el Suministro de Tokens a Través de Múltiples Cadenas?**
   * Sí, el suministro total puede distribuirse a través de múltiples cadenas al asignarlo al puente. Los tokens del suministro de la cadena de origen pueden entonces pasarse a nuevas cadenas, manteniendo la integridad del suministro total.
3. **¿Cómo Funciona la Transferencia de Suministro Entre Cadenas?**
   * Los usuarios depositan tokens en el puente, bloqueándolos en la cadena actual y seleccionando la cadena de destino para el retiro. Este proceso libera los tokens en circulación en la cadena seleccionada.
4. **¿Pueden Interactuar Contratos Externos con el Puente?**
   * Solo las direcciones fuente verificadas en cadenas verificadas pueden interactuar con el puente más allá de las funciones de usuario. Esta medida de seguridad asegura un acceso controlado a las funcionalidades del puente.
5. **¿Cuánto Cuesta?**
   * El puente tiene una tarifa plana de 1$, pero tu operación costará más porque el Puente requiere múltiples ejecuciones de contrato en 2 cadenas al mismo tiempo, lo que significa costos adicionales en tarifas de gas; por ejemplo, un depósito de BNB y puente de retiro con BASE podría costar 9$ en total, pero estos costos variarán para ti dependiendo del uso de la red en ese momento.