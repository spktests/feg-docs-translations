# 🎁 Staking

<figure><img src="../../.gitbook/assets/Screenshot_18.png" alt=""><figcaption></figcaption></figure>

### Recompensas Pasivas para Titulares

Los inversores en criptomonedas siempre buscan formas de maximizar sus inversiones y generar recompensas pasivas, y el Protocolo de Staking ofrece una oportunidad para hacerlo. Permite a los titulares hacer staking de sus tokens y ganar recompensas del volumen de trading en intercambios descentralizados como PancakeSwap o Uniswap.

### Características del Contrato de Staking

<table data-card-size="large" data-column-title-hidden data-view="cards"><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Personalización del Contrato de Staking</strong></td><td>Los propietarios pueden personalizar su staking, como tarifas de depósito y retiro, asignación de tarifas, retraso de desestakeo y recompensas adicionales.</td><td></td></tr><tr><td><strong>Distribución Automática de Recompensas</strong></td><td>Las recompensas se distribuyen y acumulan automáticamente, lo que significa que los usuarios no necesitan reclamar o reinvertir sus ganancias manualmente.</td><td></td></tr><tr><td><strong>Contrato Actualizable</strong></td><td>El contrato de staking se actualizará sin que los usuarios y propietarios del proyecto SD requieran acción.</td><td></td></tr><tr><td><strong>Fuentes de Recompensas</strong></td><td>Las recompensas pueden provenir del trading o de propietarios que también pueden inyectar manualmente otras recompensas de monedas <em>(hasta 30 recompensas separadas)</em></td><td></td></tr><tr><td><strong>Token SDSS</strong></td><td>Después de hacer staking, los usuarios reciben SD Stake Shares (SDSS) para representar la propiedad en el pool de staking. Por seguridad, SDSS no es transferible.</td><td></td></tr><tr><td><strong>Función de Sacrificio</strong></td><td>Los usuarios pueden optar por quemar un porcentaje de sus recompensas de staking al desestakear para ayudar a disminuir la oferta circulante de tokens.</td><td></td></tr><tr><td>La flexibilidad de no tener período de bloqueo te permite desestakear cuando quieras, o el desarrollador de un proyecto y elegir un período personalizado para su proyecto.</td><td></td><td></td></tr><tr><td>El desarrollador puede decidir si su proyecto tendrá un depósito y retiro o no, para adaptarse mejor a su tokenómica.</td><td></td><td></td></tr></tbody></table>

### **Fuente y Distribución de Recompensas de Staking**

Las recompensas de staking se derivan de actividades de trading en cadena de proyectos SmartDeFi; se acumulan automáticamente y están disponibles para el usuario en cualquier momento.\
\
Además, el propietario del proyecto puede inyectar manualmente otras recompensas de tokens/monedas para enviar a los stakers.\
Otras recompensas de tokens se distribuyen en rondas y están sujetas a un cierto umbral de acumulación. Los desarrolladores pueden modificar el umbral de acumulación para las recompensas, que puede diferir para cada tipo de recompensa.\
\
Por ejemplo, si 1 wBNB es el umbral, las recompensas se distribuyen cuando el pool de recompensas acumula 1 wBNB.

{% hint style="warning" %}
Desestakear o añadir al pool de staking dentro de los primeros 30 días del staking inicial resultará en una pérdida del 50% de las recompensas.\
\- Dichas recompensas perdidas se distribuirán entre otros participantes.
{% endhint %}

### **¿Qué es SDSS?**

Tras hacer staking, tus tokens SD se depositarán en el contrato de staking y, a cambio, recibirás nuevos tokens llamados SmartDeFi Stake Shares (SDSS). Estas acciones representan tu propiedad en el pool de staking. Piensa en SDSS como un recibo del sistema para confirmar que has realizado el staking exitosamente. Necesitarás mostrar este recibo al sistema para que te permita desestakear y devolverte tus tokens SD.

* SDSS no es una proporción 1:1
* SDSS se actualiza con cada recompensa de token ganada
* Total SDSS / Total SD = Proporción
* Es imposible transferir SDSS a otra billetera.

### "Sacrificio" Opcional

La función de sacrificio fue introducida en el nuevo contrato de Staking a petición de la comunidad para aquellos que deseen ayudar con los esfuerzos de quema y disminuir la oferta circulante de tokens.

Al desestakear, los stakers pueden quemar un porcentaje especificado de sus recompensas de staking, eliminándolos efectivamente de la oferta circulante.

Para activar esto, debes especificar el porcentaje a sacrificar y la cantidad a desestakear.

{% hint style="success" %}
En cualquier momento antes de desestakear, puedes desactivar el sacrificio configurándolo al 0% en la configuración de Sacrificio.
{% endhint %}