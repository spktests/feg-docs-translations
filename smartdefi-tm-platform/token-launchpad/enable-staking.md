# 🪙 Habilitar Staking

{% embed url="https://www.youtube.com/watch?v=_UvAYmQXnEc" %}

{% hint style="success" %}
Nota: estructura de tarifas para usar el Protocolo de Staking de SmartDeFi:

* Hay una tarifa de 100$ en tokens FEG que se requerirá para que los propietarios de proyectos puedan desplegar el contrato de staking (valor de la tarifa FEG a anunciar). Los tokens FEG se quemarán durante el despliegue. El costo de 100$ de FEG se determinará durante el despliegue y dependerá del precio de mercado.
* Hay una tarifa del 1% para los participantes que ingresan al staking. El % se distribuirá a los participantes de FEG, lo que permite expandir la lista de titulares y aumentar la exposición de su proyecto.
{% endhint %}

## **Desplegar Staking**

<figure><img src="../../.gitbook/assets/deploy staking UI.jpg" alt=""><figcaption></figcaption></figure>

Después de haber acuñado tus nuevos tokens, puedes habilitar la función de staking para tu proyecto, permitiendo así que tus inversionistas participen en staking con sus tokens y ganen más recompensas pasivamente del impuesto de staking.\
\
El primer paso es elegir un nombre y un símbolo para tu sistema de staking y luego hacer la aprobación, lo cual comprará y quemará una cantidad X de FEG _(cantidad final aún no decidida)_ como tarifa de servicio, luego haz clic en "Crear Staking" y acepta las solicitudes que tu aplicación de billetera necesite.&#x20;

Después, pasarás al paso 2 donde deberías ver una multitud de opciones para personalizar tu contrato de staking. Puedes profundizar en ellas y editar ahora, o simplemente editarlas más tarde cuando te sea conveniente. Si todo está bien para ti, ahora puedes proceder a hacer clic en el botón "Habilitar Staking" para lanzar el sistema de staking públicamente para tus inversionistas.

## Personalizar el contrato de staking

El sistema SmartDeFi fue construido con la personalización en mente, de modo que el sistema te permitirá editar bastantes opciones relacionadas con tu contrato de staking y puedes hacerlo tanto antes como después de lanzar tu contrato de staking, dándote así la libertad de editar el staking según lo necesites y cuantas veces quieras, basándote en los requisitos cambiantes de tu proyecto y las necesidades de tu comunidad.

### Tarifas de depósito y retiro

<figure><img src="../../.gitbook/assets/deposit and withdrawal fees.jpg" alt=""><figcaption></figcaption></figure>

Puedes optar por establecer un par de impuestos que tus inversionistas tendrían que pagar cuando depositen fondos en staking o al retirar fondos. Este impuesto puede ser de hasta el 10% de los fondos que los usuarios staken o retiren, o puedes dejarlo en 0 si lo deseas.\
Ten en cuenta que, si por ejemplo la tarifa de retiro se estableció en un 2% en el momento en que un usuario participó, incluso si luego cambias el impuesto y lo aumentas\* al 10%, el sistema recordará el nivel de impuesto original para ese usuario en particular, por lo que aún tendrá una tarifa de retiro del 2%. Tu impuesto aumentado solo se aplicará a nuevos usuarios/participantes, no a los antiguos. Dicho esto, si tu nuevo impuesto realmente reduce\* el impuesto del 2% a, por ejemplo, 1%, entonces ese nuevo impuesto se aplica tanto a los antiguos como a los nuevos participantes.&#x20;

### Asignación de tarifas de staking

<figure><img src="../../.gitbook/assets/set staking fee allocation.jpg" alt=""><figcaption></figcaption></figure>

Si has decidido habilitar un impuesto de depósito o retiro, también puedes elegir para qué usar dichos impuestos y eso te da dos opciones, puedes asignar esos ingresos a tus participantes o puedes quemarlos, aumentando así la tasa de quema de tu proyecto deflacionario.

### Retraso de Retiro

<figure><img src="../../.gitbook/assets/mature unstake delay.jpg" alt=""><figcaption></figcaption></figure>

El contrato te permite establecer un retraso personalizado para que los usuarios no puedan retirar durante los próximos X días después de haber participado por primera vez, o puedes dejarlo como está y la gente puede entrar y salir como quiera.\
Primero, deberás hacer clic en el botón "habilitar retraso" y luego podrás elegir el número deseado de días para bloquear a las personas de retirar y finalmente hacer clic en "establecer retraso" para activar la nueva configuración.

### Activar Sacrificio para tu Staking

<figure><img src="../../.gitbook/assets/set reward sacrifice.jpg" alt=""><figcaption></figcaption></figure>

La función de sacrificio se introdujo en el nuevo contrato de Staking a solicitud de la comunidad para aquellos que deseen ayudar con los esfuerzos de quema y disminuir la oferta de tokens en circulación.\
Cuando esta opción sea habilitada por ti, el desarrollador, los participantes pueden elegir quemar un porcentaje personalizado que eligen de sus recompensas de staking en el momento en que retiren o reclamen recompensas.\
El sacrificio está configurado al 0% por defecto, de modo que los usuarios puedan decidir personalmente cuánto les gustaría quemar, si es que desean quemar algo.

### Recompensas adicionales inyectadas manualmente

<figure><img src="../../.gitbook/assets/add reward token staking.jpg" alt=""><figcaption></figcaption></figure>

El contrato te permite como desarrollador del proyecto dar a tus participantes recompensas adicionales, lo cual puedes hacer inyectándolas manualmente desde tu propia billetera.\
Por ejemplo, digamos que tienes un ingreso adicional de BNB de un juego o lo que sea, puedes tomar ese BNB y inyectarlo en el contrato de staking, el cual luego dividirá dicho BNB entre todos los participantes y todos recibirán su parte de ese BNB como recompensas de staking. \
También puedes elegir el umbral de distribución cuando el sistema comenzará a distribuir dicho BNB entre tus participantes, por ejemplo, puedes decirle al sistema que solo distribuya las recompensas en BNB una vez que tengas 1+ BNB inyectado en el pool, para que puedas inyectar fondos en lotes más pequeños a lo largo del tiempo, pero el sistema no auto-distribuirá hasta que el umbral establecido se alcance.\

### Impulsar tu Respaldo de Activos usando las recompensas

Si tu SD_token tiene el mismo token configurado para respaldo de activos y también como recompensa adicional, por ejemplo, wBNB, entonces esta opción permitirá que el contrato tome un porcentaje de la recompensa adicional y envíe esa parte al pool de respaldo del token en lugar de enviarlo como recompensa para los participantes.\
Esta opción se llama "SetBoostBacking" y por ahora se puede encontrar en SDscan > Staking > Interface > Write, y en esa lista será la opción #9. Puedes ingresar cualquier valor entre 0 a 100% y luego hacer clic en el botón "write" para activar la edición.