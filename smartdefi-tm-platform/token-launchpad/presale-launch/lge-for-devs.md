# 👤 LGE para Desarrolladores

{% hint style="info" %}
Esta página está siendo actualizada con las últimas implementaciones&#x20;
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=7SpIEcXtqYY" %}

Supongamos que no tienes los fondos privados para añadir liquidez a tu proyecto SmartDeFi, en ese caso, puedes reunir liquidez de inversores utilizando el sistema de Evento de Generación de Liquidez, LGE por sus siglas en inglés, o conocido como _"preventa"_ para la gente sencilla como yo.

## Paso 1 - Desplegar el LGE

<figure><img src="../../../.gitbook/assets/deploy LGE jan.jpg" alt=""><figcaption></figcaption></figure>

Como habrás notado, el Desplegador LGE tiene bastantes opciones para que personalices, así que vamos rápidamente a revisarlas:

**• Tokens para LGE**  (cantidad de tokens SD)\
Aquí, puedes decidir cuántos de tus tokens SD deseas dar para la preventa. Se aconseja que pongas el 100% del suministro.

**• Tasa**  (tokens SD por BNB)\
La cantidad de tokens que elijas aquí decidirá el precio al que las personas comprarán tu token durante la preventa e inmediatamente después.\
\- Nota: Cualquier configuración que elijas en el campo "Porcentaje de Reserva" también afectará el precio.

**• Compra máxima**  (BNB/ETH)\
La cantidad máxima de BNB/ETH que los inversores pueden usar para comprar en tu preventa.

**• Fecha y hora de inicio** \
Puedes seleccionar un día y una hora exactos cuando la preventa puede activarse y ejecutarse.

**• Duración** (Días)\
El número de días que deseas que tu preventa se ejecute antes de que cierre automáticamente.

**• Demora de liberación**  (Días)\
El sistema puede liberar liquidez bloqueada en lotes, y puedes decidir cuántos días tener entre cada lote.

**• Tasa de liberación**  (%)\
Puedes decidir cuánto de la liquidez bloqueada liberar durante cada fase de desbloqueo de lotes.

**• Porcentaje de Reserva** (%)\
Cuando el LGE finaliza la preventa, un porcentaje del BNB/ETH reunido puede ser inyectado en la reserva de activos para crear un token más estable. Se aconseja poner el 50% para que una vez liberado, el precio del token sea inicialmente similar a su valor de respaldo de activos.

**• Porcentaje para el Desarrollador** (%)\
El sistema puede dar al propietario de SD un porcentaje de la liquidez y liberarlo, tal como se libera para los inversores regulares. El proyecto puede usar esta parte para lo que necesiten, como marketing, listados CEX, etc.

**• Porcentaje FEG** (%)\
El sistema colocará el BNB/ETH reunido en dos pools de liquidez, uno para SD/BNB y otro para SD/FEG. Puedes elegir cómo dividir estos dos pools de liquidez. Esto también asegura que tus inversores tengan una oportunidad para el arbitraje desde el principio, lo que genera más ingresos para ti a través de impuestos.

Ahora que has elegido todas tus configuraciones preferidas para el LGE, es hora de presionar el botón "_Aprobar_" en la parte inferior, aceptar las aprobaciones que recibas de tu aplicación de cartera y cubrir los costos de gas de la cadena de bloques requeridos para la ejecución de la transacción.\
\
Una vez hecho esto, verás un nuevo botón llamado "_Desplegar_", haz clic en él y acepta las aprobaciones de la cartera, y luego eso es todo, tu LGE ahora está desplegado y listo para funcionar según las configuraciones que elegiste.

### 1.1 Editar el LGE antes de que se active

<figure><img src="../../../.gitbook/assets/edit presale after.jpg" alt=""><figcaption></figcaption></figure>

Una vez que creas la preventa, tienes un período de gracia en el que aún puedes editarla antes de que realmente comience. \
En el tablero de tu token, haz clic en "Editar LGE" y eso abrirá un nuevo menú emergente donde notarás todas las configuraciones que hiciste anteriormente y también al lado de cada una habrá un botón de "editar", haz clic en él y esto te permitirá editar lo que necesites.\
Recuerda que no puedes realizar ediciones una vez que la preventa ha comenzado y está en vivo.

### 1.2 Lista blanca de direcciones para la preventa

<figure><img src="../../../.gitbook/assets/whitelist address.jpg" alt=""><figcaption></figcaption></figure>

Cuando editas la preventa, antes de que se active, tienes la opción de añadir una lista blanca a tu preventa, lo que significa que puedes añadir un número de direcciones de cartera que son VIPs y que tendrán un lugar asegurado en la preventa una vez que esté en vivo, lo que significa que la preventa estará bloqueada para el público en general, hasta que los VIPs compren en la preventa. \
Cada VIP solo puede invertir en la preventa la misma cantidad de ETH/BNB que cualquier otro usuario puede, por lo que la cantidad máxima tiene el mismo límite para todos.\
Primero necesitarás habilitar la lista blanca, luego añades las direcciones que deseas y finalmente haces clic en el botón "lista blanca de direcciones".\
Después de que todas las direcciones en lista blanca compren en la preventa, la preventa se abrirá automáticamente al público en general y todos podrán comenzar a invertir.\
La preventa estará bloqueada hacia el público hasta que TODAS las direcciones en lista blanca compren en la preventa.\
Tú como desarrollador también puedes eliminar personas de la lista blanca, si lo necesitas. También puedes deshabilitar la lista blanca por completo si así lo decides, algún tiempo después de haberla habilitado, si por ejemplo una de las carteras en lista blanca se queda inactiva y no compra en la preventa, manteniendo así bloqueada la preventa para los usuarios promedio. Así que tienes la opción de expulsar personas de la lista blanca o deshabilitarla por completo, si tienes tales problemas con uno o más usuarios.

## Paso 2 - Finalizar el LGE y lanzar el proyecto

Si tú como el DESARROLLADOR no abres el comercio dentro de las 72 horas después de que finalice el LGE, entonces tus inversores podrán cancelar su participación en el LGE y pueden recuperar sus fondos invertidos.

Si el límite de 72h pasa y las personas comienzan a retirar su dinero del pool de preventa y si la cantidad cae por debajo del softcap, el DESARROLLADOR todavía podrá lanzar el proyecto para el comercio.

La preventa puede finalizar de 3 maneras:

### 2.1 Preventa agotada y el Hardcap fue alcanzado

Si lograste reunir todo el BNB que te propusiste recaudar, entonces tu preventa terminará en el momento en que se alcance ese hardcap, independientemente de si esto ocurre apenas 1 día después de que comenzó la preventa y tu límite de tiempo inicial fue establecido para 90 días.\
Una vez que finalice la preventa, tú como el DESARROLLADOR necesitarás abrir manualmente el comercio a través de nuestra interfaz de usuario, momento en el cual el sistema configurará automáticamente tus pools de liquidez en Pancakeswap para BNB o en Uniswap para ETH y BASE.\
Después de eso, tú o tus inversores necesitarán ir a la página de la preventa en FEGex y hacer clic en el botón "Habilitar acciones" para que tus inversores puedan comenzar a reclamar sus acciones según tu calendario establecido.

### 2.2 La preventa termina y solo se alcanza el Softcap

<figure><img src="../../../.gitbook/assets/closed with softcap (1).jpg" alt=""><figcaption></figcaption></figure>

Una vez que se alcanza el límite de tiempo de la preventa y se ha logrado reunir la cantidad necesaria para el softcap, se considera que la preventa ha sido exitosa y se colocará en la subcategoría "Completado".\
En este punto, cualquier persona (inversor o no) puede venir y hacer clic en "Forzar fin de preventa".\
El sistema configurará automáticamente tus pools de liquidez en Pancakeswap para BNB o en Uniswap para ETH y BASE.\
Después de eso, tú o tus inversores necesitarán ir a la página de la preventa en FEGex y hacer clic en el botón "Habilitar acciones" para que tus inversores puedan comenzar a reclamar sus acciones según tu calendario establecido.

### 2.3 La preventa termina pero el Softcap NO se alcanza

<figure><img src="../../../.gitbook/assets/presale failed (1).jpg" alt=""><figcaption></figcaption></figure>

La preventa será automáticamente movida a la subcategoría "Fallido" si tu límite de tiempo ha sido alcanzado pero no lograste reunir suficientes fondos para el softcap.\
En este punto, cualquier inversor puede hacer clic en el botón "Abortar preventa" y luego en el botón "Salir de la preventa", al hacer clic en esto, hará que tus fondos en la preventa regresen a tu cartera, en forma de BNB/ETH env