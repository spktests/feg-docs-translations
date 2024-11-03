# 🪙 Habilitar Staking

{% embed url="https://www.youtube.com/watch?v=_UvAYmQXnEc" %}

{% hint style="success" %}
Nota: estructura de tarifas para usar el Protocolo SmartDeFi Staking:

* Hay una tarifa de $100 en tokens FEG que se requerirá para que los propietarios de proyectos puedan desplegar el contrato de staking (valor de la tarifa FEG por anunciar). Los tokens FEG se quemarán durante el despliegue. El costo de $100 de FEG se determinará durante el despliegue y dependerá del precio de mercado.
* Hay una tarifa del 1% para los stakers de tokens al ingresar al staking. El porcentaje será distribuido a los stakers de FEG, lo cual permite expandir la lista de holders y aumentar la exposición de tu proyecto.
{% endhint %}

## **Desplegar Staking**

<figure><img src="../../.gitbook/assets/deploy staking UI.jpg" alt=""><figcaption></figcaption></figure>

Después de que hayas acuñado tus nuevos tokens, puedes habilitar la función de staking para tu proyecto, permitiendo así que tus inversores hagan staking de sus tokens y obtengan más recompensas pasivamente del impuesto de staking.\
\
El primer paso es elegir un nombre y un símbolo para tu sistema de staking y luego hacer la aprobación, lo cual comprará y quemará X cantidad de FEG _(cantidad final aún no decidida)_ como tarifa de servicio, luego haz clic en "Create Stake" y acepta cualquier solicitud que necesite tu aplicación de billetera.&#x20;

Después, pasarás al paso 2 donde deberías ver una multitud de opciones para personalizar tu contrato de staking. Puedes profundizar en ellas y editarlas ahora, o simplemente editarlas más tarde cuando te convenga. Si todo está correcto para ti, ahora puedes proceder a hacer clic en el botón "Enable Staking" para lanzar el sistema de staking públicamente para tus inversores.

## Personalizar contrato de staking

El sistema SmartDeFi fue construido pensando en la personalización, por lo que el sistema te permitirá editar bastantes opciones relacionadas con tu contrato de staking y puedes hacerlo tanto antes como después de lanzar tu contrato de staking, dándote la libertad de editar el staking según sea necesario siempre que quieras y tantas veces como quieras, basado en los requisitos en evolución de tu proyecto y las necesidades de tu comunidad.

### Tarifas de depósito y retiro

<figure><img src="../../.gitbook/assets/deposit and withdrawal fees.jpg" alt=""><figcaption></figcaption></figure>

Puedes optar por establecer un par de impuestos que tus inversores tendrían que pagar cuando depositen fondos en el staking o cuando retiren fondos. Este impuesto puede ser de hasta el 10% de los fondos que los usuarios staken o des-staken, o puedes simplemente dejarlo en 0 si lo deseas.\
Ten en cuenta que si, por ejemplo, la tarifa de retiro se estableció en un 2% en el momento en que un usuario hizo staking, incluso si más tarde cambias el impuesto y lo aumentas\* al 10%, el sistema recordará el nivel de imposición original para ese usuario en particular, por lo que aún tendrán un 2% de tarifa de retiro. Tu impuesto aumentado solo se aplicará para nuevos usuarios/stakers, no para stakers antiguos. Dicho esto, si tu nuevo impuesto de hecho disminuye\* el impuesto del 2% a, por ejemplo, el 1%, entonces ese nuevo impuesto se aplica tanto para stakers antiguos como nuevos.&#x20;

### Asignación de tarifa de staking

<figure><img src="../../.gitbook/assets/set staking fee allocation.jpg" alt=""><figcaption></figcaption></figure>

Si has decidido habilitar un impuesto de depósito o retiro, también puedes elegir para qué usar estos impuestos y eso te da dos opciones: puedes asignar esos ingresos a tus stakers o puedes quemarlos, aumentando así la tasa de quema de tu proyecto deflacionario.

### Retraso para Des-stakear

<figure><img src="../../.gitbook/assets/mature unstake delay.jpg" alt=""><figcaption></figcaption></figure>

El contrato te permite configurar un retraso personalizado para que los usuarios no puedan des-stakear durante los próximos X días después de que hayan hecho staking por primera vez, o puedes simplemente dejarlo como está y la gente podrá entrar y salir cuando lo desee.\
Primero tendrás que hacer clic en el botón "enable delay" y luego puedes elegir el número deseado de días para bloquear a las personas de des-stakear y finalmente hacer clic en "set delay" para activar la nueva configuración.

### Activar Sacrificio para tu Staking

<figure><img src="../../.gitbook/assets/set reward sacrifice.jpg" alt=""><figcaption></figcaption></figure>

La función de sacrificio se introdujo en el nuevo contrato de Staking a solicitud de la comunidad para aquellos que deseen ayudar con los esfuerzos de quema y disminuir el suministro de tokens circulantes.\
Cuando esta opción es habilitada por ti, el desarrollador, los stakers pueden elegir quemar un porcentaje personalizado que elijan de sus recompensas de staking en el momento en que des-stakeen o reclamen recompensas..\
El sacrificio se establece en 0% por defecto, de modo que los usuarios pueden decidir personalmente cuánto les gustaría quemar, si es que deciden quemar algo.

### Recompensas adicionales inyectadas manualmente

<figure><img src="../../.gitbook/assets/add reward token staking.jpg" alt=""><figcaption></figcaption></figure>

El contrato te permite, como desarrollador del proyecto, dar a tus stakers recompensas adicionales, las cuales puedes inyectar manualmente desde tu propia billetera.\
Por ejemplo, digamos que tienes un ingreso adicional de BNB de un juego o lo que sea, puedes tomar ese BNB e inyectarlo en el contrato de staking, que luego dividirá dicho BNB entre todos los stakers y todos recibirán su parte de ese BNB como recompensas de staking. \
También puedes elegir el umbral de distribución cuando el sistema comenzará a distribuir dicho BNB entre tus stakers, por lo que, por ejemplo, puedes decirle al sistema que solo distribuya las recompensas de BNB una vez que hayas inyectado 1+ BNB en el pool, por lo que puedes inyectar fondos en lotes más pequeños con el tiempo pero el sistema no auto-distribuirá hasta que se alcance el umbral establecido.\


### Aumenta tu Respaldo de Activos usando los tokens de recompensa

Si tu SD\_token tiene el mismo token configurado para respaldo de activos y también como recompensa adicional, por ejemplo wBNB, entonces esta opción permitirá al contrato tomar un porcentaje del premio adicional y enviar esa parte al pool de respaldo de tokens en lugar de enviarlo como recompensa para stakers.\
Esta opción se llama "SetBoostBacking" y por ahora se puede encontrar en SDscan > Staking > Interface > Write y en esa lista será la opción #9. Puedes ingresar cualquier cosa entre 0 al 100% y luego hacer clic en el botón "write" para activar la edición.