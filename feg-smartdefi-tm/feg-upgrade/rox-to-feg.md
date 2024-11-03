# ↔️ ROX a FEG

### El Plan de Consignación&#x20;

En 2022, decidimos fusionar ROX con FEG para simplificar nuestro ecosistema y aumentar el valor para nuestros inversionistas. Todos los poseedores de ROX han recibido tokens FEG a cambio. Estos tokens pueden ser reclamados durante un período de adquisición de 25 meses, con un 4% de sus participaciones liberadas mensualmente. Los inversores tienen la flexibilidad de reclamar su 4% mensual o acumular sus reclamaciones, por ejemplo, durante 5 meses para reclamar el 20% de una vez, minimizando así las tarifas de gas.

{% hint style="warning" %}
Las reclamaciones no están sujetas a impuestos, sin embargo, SÍ debes pagar las tarifas de gas de la blockchain para ejecutar transacciones, así que tenlo en cuenta, especialmente en ETH.
{% endhint %}

### Reclamaciones

Lote más reciente: la reclamación #4 del 4% se liberó el 1 de septiembre de 2024.

Lotes liberados hasta ahora que puedes reclamar en una sola transacción: 16%.

### La proporción de ROX a FEG&#x20;

BSC → 1 ROX = 3,812,101.67910245 FEG\
ETH → 1 ROX = 3,412,864.15305551 FEG\
También puedes usar [https://calc.fegtoken.com/](https://calc.fegtoken.com/) para facilitarlo.

### Cómo actualizar ROX a FEG

<figure><img src="../../.gitbook/assets/ROX to FEG.jpg" alt=""><figcaption></figcaption></figure>

Visita SmartDeFi.com y conecta tu billetera. Haz clic en la pestaña "Upgrader" en la página de FEG, luego selecciona la pestaña "ROX Convert". Aquí verás el número de tokens ROX vinculados a tu billetera y la cantidad de nuevos FEG que recibirás a cambio.\
Para completar la actualización, haz clic en el botón "Aprobar", luego en el botón "Actualizar".

### Nota: también puedes Actualizar + Puente

Si lo deseas, puedes hacer que tus nuevos FEG sean entregados o puenteados a otra cadena, como BASE, por ejemplo. Esto significa que el actualizador convertirá tus tokens ROX antiguos en la cadena actual y desbloqueará los nuevos FEG en tu cadena elegida.\
Para iniciar el proceso de actualización, elige tu cadena deseada, haz clic en el botón "Aprobar", luego en el botón "Actualizar".

Para retirar tus nuevos FEG en la cadena elegida, primero cambia la red en tu billetera, ve a la pestaña "Puente", luego a la pestaña "Retiros", y haz clic en el botón "Retirar".

<figure><img src="../../.gitbook/assets/withdraw upgraded FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Recuerda, necesitas monedas nativas para tarifas de gas en las cadenas de origen y destino.

¡Las tarifas de gas por el uso del puente son más altas que las transacciones normales!
{% endhint %}

¡Y eso es todo! Has actualizado con éxito de ROX a FEG y puenteado a otra cadena en tan solo unos clics. Es simple y fácil.

### Direcciones antiguas de ROX

```
ROX on BSC // 0xa3D522c151aD654b36BDFe7a69D0c405193A22F9
```

```
ROX on ETH // 0x378c77C5379cA07BBB5B3506c08a1C769dEC91c2
```

## Preguntas Frecuentes

### ¿Las reclamaciones son automáticas o manuales?

Es manual, y necesitas usar la herramienta de actualización en [SmartDeFi.com](https://smartdefi.com) para reclamar tu FEG.

### ¿Cómo recibo FEG?

En cada reclamación, tienes 3 opciones relacionadas con dónde recibir los nuevos FEG:

1. reclamar FEG en una billetera en la cadena actual
2. reclamar FEG en una billetera en la cadena de tu elección (BSC/ETH/BASE)
3. reclamar y auto-estacar en la cadena actual

### ¿Cómo se calculó la proporción de ROX y FEG?

Establecimos la proporción usando los precios de apertura de FEG y ROX el 15 de mayo de 2022. El valor de ROX y FEG se calculó dividiendo el número de monedas nativas (ETH o BNB) pagadas por el número de tokens (FEG o ROX) recibidos. Para determinar cuántos FEG rinde un ROX, dividimos el valor en monedas nativas de un ROX por el valor en monedas nativas de un FEG. En términos simples, esta proporción representa la cantidad de FEG que podrías haber comprado por el mismo precio que un ROX.

Transacciones Abiertas de BSC\
**ROX**: 0x1a0e998a173ef8b395513f85a44b5abd8db2c9f7a79daf19f477165015843504\
**FEG**: 0x190b55b45916e4c79a98d061d2edd16c8cf67f119fa3544e0273e6f6b6ee1cd0

Transacciones Abiertas de ETH\
**ROX**: 0x883c756fe5be2182b5e45f80286f8d4c7e2eea23eebe1e15ea53d66932aee026\
**FEG**: 0x0f58396870514f4419ed542dfada345b299971a43f186f1bfc6ea8d29c838bd5\
\* Nota: El 15 de mayo, SOLO se usó una transacción de ROX ETH como precio de apertura.

### ¿Por qué usar valores pre-exploit en lugar de post-exploit para FEG?

Usar variables pre-exploit para ambos tokens fue considerado el enfoque más lógico, esencialmente creando una "instantánea" de las condiciones del mercado antes de que ocurriera cualquier exploit. Aunque ROX habría enfrentado las mismas condiciones de mercado que FEG post-exploit, evitamos especular sobre precio y suministro circulante. En cambio, confiamos en datos puros de la blockchain en lugar de cifras arbitrarias.

### ¿Por qué no usar los grupos de liquidez de ROX y FEG para determinar la proporción?

Decidimos no usar este método por dos razones principales:

1\. FEG no tenía un LP respaldado por activos como ROX. Mientras que ROX se benefició de tener tanto un LP respaldado por activos como un LP de mercado, FEG solo tenía un LP de mercado. Por lo tanto, usar LPs para determinar la proporción hubiera sido injusto, ya que FEG no pudo aprovechar la misma tecnología de respaldo de activos que benefició a ROX.

2\. Para evitar diluir en gran medida a los inversores de FEG, consideramos el LP total para ambos tokens. El LP para ROX BSC era aproximadamente 2.23 veces mayor que para FEG BSC, y el LP para FEG ETH era aproximadamente 1.42 veces mayor que para ROX ETH. Usando estas métricas, los poseedores de ROX BSC habrían poseído el 69% del nuevo suministro de FEG V2, y los poseedores de ROX ETH habrían poseído el 41%. Una discrepancia de propiedad tan significativa a través de las cadenas hubiera sido injusta para los poseedores de FEG y podría haber puesto en riesgo el proyecto.

· LPs de BSC → ROX = 5672 BNB; FEG = 2544 BNB

· LPs de ETH → ROX = 425 ETH; FEG = 604 ETH