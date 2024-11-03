# 👤 LGE para Desarrolladores

{% hint style="info" %}
Esta página se está actualizando con las últimas implementaciones&#x20;
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=7SpIEcXtqYY" %}

Supongamos que no tienes los fondos privados para añadir liquidez a tu proyecto de SmartDeFi, en ese caso, puedes reunir liquidez de inversores utilizando el sistema de Evento de Generación de Liquidez, LGE por sus siglas en inglés, o conocido como _"presale"_ para la gente simple como yo.

## Paso 1 - Desplegar el LGE

<figure><img src="../../../.gitbook/assets/deploy LGE jan.jpg" alt=""><figcaption></figcaption></figure>

Como habrás notado, el Desplegador de LGE tiene bastantes opciones para que personalices, así que vamos a repasarlas rápidamente:

**• Tokens para LGE**  (cantidad de SD-tokens)\
Aquí, puedes decidir cuántos de tus SD-tokens deseas asignar para la preventa. Se recomienda asignar el 100% del suministro.

**• Tasa**  (SD-tokens por BNB)\
La cantidad de tokens que elijas aquí decidirá el precio que la gente pagará por tu token durante la preventa e inmediatamente después.\
\- Nota: Cualquier configuración que elijas en el campo "Participación de respaldo" también afectará el precio.

**• Máxima compra**  (BNB/ETH)\
La cantidad máxima de BNB/ETH que los inversores pueden usar para comprar en tu preventa.

**• Fecha y hora de inicio**\
Puedes elegir un día y hora exactos cuando la preventa puede activarse y ejecutarse.

**• Duración** (Días)\
El número de días que deseas que tu preventa dure antes de que se cierre automáticamente.

**• Retardo de adquisición**  (Días)\
El sistema puede liberar la liquidez bloqueada en lotes, y puedes decidir cuántos días habrá entre cada lote.

**• Tasa de adquisición**  (%)\
Puedes decidir cuánta de la liquidez bloqueada se liberará durante cada fase de desbloqueo de lotes.

**• Participación de respaldo** (%)\
Cuando termine la LGE, un porcentaje del BNB/ETH recaudado puede ser inyectado en el respaldo de activos para crear un token más estable. Se aconseja colocar el 50% para que una vez lanzado, el precio del token sea inicialmente similar a su valor de respaldo de activos.

**• Participación del desarrollador** (%)\
El sistema puede dar al propietario de SD un porcentaje de la liquidez y adquirirlo, al igual que se adquieren para los inversores regulares. El proyecto puede usar esta participación para lo que necesiten, como marketing, listados de CEX, etc.

**• Participación de FEG** (%)\
El sistema colocará el BNB/ETH reunido en dos fondos de liquidez, uno para SD/BNB y otro para SD/FEG. Puedes elegir cómo dividir estos dos fondos de liquidez. Esto también asegura que tus inversores tengan una oportunidad de arbitraje desde el principio, lo que significa más ingresos para ti a través de impuestos.

Una vez que hayas elegido todas tus configuraciones preferidas para el LGE, es el momento de pulsar el botón "_Aprobar_" en la parte inferior, acepta cualquier aprobación que recibas de tu aplicación de billetera y cubre las tarifas de gas de la blockchain necesarias para la ejecución de la transacción.\
\
Una vez hecho esto, verás un nuevo botón llamado "_Desplegar_" haz clic en él y acepta las aprobaciones de la billetera, y eso es todo, tu LGE ahora está desplegado y listo para funcionar según las configuraciones que elegiste.

### 1.1 Editar el LGE antes de que se active

<figure><img src="../../../.gitbook/assets/edit presale after.jpg" alt=""><figcaption></figcaption></figure>

Una vez que crees la preventa, tienes un período de gracia donde todavía puedes editarla antes de que realmente comience.\
En el tablero de tu token, haz clic en "Editar LGE" y se abrirá un nuevo menú emergente donde notarás todas las configuraciones que hiciste anteriormente y también junto a cada una habrá un botón de "editar", haz clic en él y esto te permitirá editar lo que necesites.\
Recuerda que no puedes realizar ninguna edición una vez que la preventa ha comenzado y está en vivo.

### 1.2 Listado de direcciones para preventa

<figure><img src="../../../.gitbook/assets/whitelist address.jpg" alt=""><figcaption></figcaption></figure>

Cuando editas la preventa, antes de que se active, tienes la opción de añadir una lista de direcciones a la preventa, lo que significa que puedes añadir un número de direcciones de billeteras que son VIPs y que tendrán un lugar asegurado en la preventa una vez que se active, lo que significa que la preventa estará bloqueada para el público general, hasta que los VIPs compren en la preventa.\
Cada VIP solo puede invertir en la preventa la misma cantidad de ETH/BNB que cualquier otro usuario, por lo que la cantidad máxima tiene el mismo límite para todos.\
Primero necesitarás habilitar la lista de direcciones, luego añades las direcciones que desees y finalmente haces clic en el botón "las direcciones de la lista".\
Después de que todas las direcciones de la lista compren en la preventa, la preventa se abrirá automáticamente al público general y todos pueden comenzar a invertir.\
La preventa estará bloqueada hacia el público hasta que TODAS las direcciones de la lista compren en la preventa.\
Tú como desarrollador también puedes eliminar personas de la lista, si lo necesitas. También puedes deshabilitar la lista completamente si decides hacerlo, algún tiempo después de haberla habilitado, por ejemplo, si una de las billeteras de la lista queda inactiva y no compra en la preventa, manteniendo así la preventa bloqueada para los usuarios promedio. Por lo tanto, tienes la opción de eliminar personas de la lista o deshabilitarla por completo, si tienes tales problemas con uno o más usuarios.

## Paso 2 - Finalización del LGE y lanzamiento del proyecto

Si como DESARROLLADOR no abres el comercio dentro de las 72 horas posteriores al final del LGE, entonces tus inversores podrán cancelar su participación en el LGE y podrán recuperar sus fondos invertidos.

Si el límite de 72h pasa y la gente comienza a retirar su dinero del fondo de preventa y si la cantidad cae por debajo del softcap, el DESARROLLADOR todavía podrá lanzar el proyecto para el comercio.

La preventa puede terminar de 3 maneras:

### 2.1 Preventa agotada y se alcanzó el Hardcap

Si lograste reunir todos los BNB que te propusiste recaudar, entonces tu preventa terminará en el momento en que se alcance el hardcap, independientemente de si esto sucede apenas 1 día después de que la preventa comenzara y tu límite de tiempo inicial se estableció para 90 días.\
Una vez que la preventa termine, tú como DESARROLLADOR necesitarás abrir manualmente el comercio a través de nuestra interfaz de usuario, momento en el que el sistema configurará automáticamente tus fondos de liquidez en Pancakeswap para BNB o en Uniswap para ETH y BASE.\
Después de eso, tú o tus inversores necesitarán ir a la página de la preventa en FEGex y hacer clic en el botón "Habilitar acciones" para que tus inversores puedan comenzar a reclamar sus acciones según tu calendario establecido.

### 2.2 La preventa termina y solo se alcanza el Softcap

<figure><img src="../../../.gitbook/assets/closed with softcap (1).jpg" alt=""><figcaption></figcaption></figure>

Una vez que se alcanza el límite de tiempo de la preventa y se ha logrado reunir la cantidad necesaria para el softcap, se considera que la preventa es exitosa y se colocará en la subcategoría "Completado".\
En este punto cualquiera (inversor o no) puede venir y hacer clic en "Forzar el final de la preventa".\
El sistema configurará automáticamente tus fondos de liquidez en Pancakeswap para BNB o en Uniswap para ETH y BASE.\
Después de eso, tú o tus inversores necesitarán ir a la página de la preventa en FEGex y hacer clic en el botón "Habilitar acciones" para que tus inversores puedan comenzar a reclamar sus acciones según tu calendario establecido.

### 2.3 La preventa termina pero NO se alcanza el Softcap

<figure><img src="../../../.gitbook/assets/presale failed (1).jpg" alt=""><figcaption></figcaption></figure>

La preventa se trasladará automáticamente a la subcategoría "Fallido" si tu límite de tiempo ha llegado pero no lograste reunir suficientes fondos para el softcap.\
En este punto, cualquier inversor puede hacer clic en el botón "Abortar preventa" y luego en el botón "Salir de la preventa", al hacer clic en esto, tus fondos de preventa se devolverán a tu billetera, en forma de BNB/ETH envueltos.

### 2.4 Condiciones