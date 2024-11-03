# ⛓️ Puente Cross-chain

<figure><img src="../.gitbook/assets/Screenshot_14 (1).png" alt=""><figcaption></figcaption></figure>

Presentamos el Puente Cross-Chain On-Chain de SmartDeFi, una función revolucionaria disponible para todos los proyectos lanzados desde el Launchpad de Tokens de SmartDeFi.&#x20;

El Puente abre un mundo de posibilidades con una interoperabilidad fluida entre diferentes blockchains EVM, completamente en la cadena, donde los usuarios ahora pueden disfrutar de una flexibilidad, arbitraje y accesibilidad sin precedentes al gestionar sus tokens.&#x20;

Únete a nosotros en este emocionante viaje hacia un ecosistema más interconectado y descentralizado.

### Cómo Funciona

<figure><img src="../.gitbook/assets/bridge 1 FEG base to bnb.jpg" alt=""><figcaption></figcaption></figure>

Dirígete a [SmartDeFi.com](https://smartdefi.com), conecta tu billetera, elige el token que deseas puentear y luego haz clic en la pestaña "Bridge".&#x20;

En este punto se te dará la oportunidad de elegir a qué cadena deseas puentear, el siguiente paso es que necesitas ingresar la cantidad de tokens a puentear desde la cadena X a la cadena Y. Por último, deberás hacer clic en el botón "Aprobar" y luego en el botón "Bridge" para realizar la transacción de puenteo.

Ahora solo queda cambiar la red de tu billetera a la cadena a la que enviaste los tokens, luego asegúrate de estar en la pestaña "Bridge" y en la pestaña "Withdrawals". Revisa para asegurarte de que toda la información mostrada sea correcta y luego haz clic en el botón "Retirar".&#x20;

{% hint style="success" %}
Recuerda que necesitas monedas nativas para tarifas de gas en ambas cadenas, la de origen y la de destino.

Las tarifas de gas para el uso del puente son más altas que las transacciones normales.
{% endhint %}

Y eso es todo, has puenteado tus tokens a otra cadena en pocos clics, simple y fácil.

<figure><img src="../.gitbook/assets/withdraw bridge 1FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
El Puente está limitado a una instancia de puenteo cada 15 minutos.&#x20;

El usuario tiene hasta 30 días para reclamar los activos del SmartBridge.&#x20;

Los activos no reclamados se perderán para siempre.
{% endhint %}

### Preguntas Frecuentes

1. **¿Quién Puede Iniciar la Creación de un Puente?**
   * Solo el propietario del contrato inteligente del token de SmartDeFi puede iniciar la creación de un puente. Esto asegura el acceso autorizado y la verificación de la billetera del propietario a través de cadenas.
2. **¿Puede El Suministro de Tokens Ser Distribuido a Través de Múltiples Cadenas?**
   * Sí, el suministro total puede ser distribuido a través de múltiples cadenas al asignarlo al puente. Luego, los tokens del suministro de la cadena de origen pueden ser puenteados a nuevas cadenas, manteniendo la integridad del suministro total.
3. **¿Cómo Funciona la Transferencia de Suministro a Través de Cadenas?**
   * Los usuarios depositan tokens en el puente, los bloquean en la cadena actual y seleccionan la cadena de destino para la retirada. Este proceso libera los tokens en circulación en la cadena seleccionada.
4. **¿Pueden Contratos Externos Interactuar con el Puente?**
   * Solo direcciones de origen verificadas en cadenas verificadas pueden interactuar con el puente más allá de las funciones de usuario. Esta medida de seguridad asegura un acceso controlado a las funcionalidades del puente.
5. **¿Cuál es el costo?**
   * El puente tiene una tarifa fija de 1$, pero tu operación costará más porque el Puente requiere múltiples ejecuciones de contratos en 2 cadenas al mismo tiempo, lo que significa costos adicionales en tarifas de gas; por ejemplo, un puente de depósito BNB y retiro BASE podría costar 9$ en total, pero estos costos variarán para ti dependiendo del uso de la red en ese momento.