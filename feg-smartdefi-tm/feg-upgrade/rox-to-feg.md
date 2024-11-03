# ↔️ ROX a FEG

### El Plan de Consolidación

En 2022, decidimos fusionar ROX en FEG para simplificar nuestro ecosistema y aumentar el valor para nuestros inversores. Todos los poseedores de ROX han recibido tokens FEG a cambio. Estos tokens se pueden reclamar durante un periodo de consolidación de 25 meses, con un 4% de sus tenencias liberado mensualmente. Los inversores tienen la flexibilidad de reclamar su 4% mensual o acumular sus reclamaciones, por ejemplo, durante 5 meses para reclamar el 20% de una vez, minimizando las tarifas de gas.

{% hint style="warning" %}
Las reclamaciones no están sujetas a ningún impuesto, sin embargo, SÍ debes pagar las tarifas de gas de la blockchain para ejecutar las transacciones, así que tenlo en cuenta, especialmente en ETH.
{% endhint %}

### Reclamaciones

Último lote: la reclamación #4 del 4% se liberó el 1 de septiembre de 2024.

Lotes liberados hasta ahora que puedes reclamar en una transacción: 16%

### La proporción de ROX a FEG

BSC →  1 ROX = 3,812,101.67910245 FEG\
ETH →  1 ROX = 3,412,864.15305551 FEG\
También puedes usar [https://calc.fegtoken.com/](https://calc.fegtoken.com/) para facilitar el cálculo.

### Cómo actualizar ROX a FEG

<figure><img src="../../.gitbook/assets/ROX to FEG.jpg" alt=""><figcaption></figcaption></figure>

Visita SmartDeFi.com y conecta tu cartera. Haz clic en la pestaña "Upgrader" en la página de FEG, luego selecciona la pestaña "ROX Convert". Aquí verás el número de tokens ROX vinculados a tu cartera y el número de FEG nuevos que recibirás a cambio.\
Para completar la actualización, haz clic en el botón "Approve", luego en el botón "Upgrade".

### Nota: también puedes Actualizar + Puente

Si lo deseas, puedes recibir o transferir tus nuevos FEG a otra cadena, como BASE por ejemplo. Esto significa que el actualizador convertirá tus antiguos tokens ROX en la cadena actual y desbloqueará los nuevos FEG en la cadena que elijas. \
Para iniciar el proceso de actualización, selecciona la cadena deseada, haz clic en el botón "Approve", luego en el botón "Upgrade".

Para retirar tus nuevos FEG en la cadena elegida, primero cambia la red en tu cartera, ve a la pestaña "Bridge", luego a la pestaña "Withdrawals", y haz clic en el botón "Withdraw".

<figure><img src="../../.gitbook/assets/withdraw upgraded FEG.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Recuerda, necesitas monedas nativas para pagar las tarifas de gas en la cadena de origen y destino.

¡Las tarifas de gas por el uso del puente son más altas que las transacciones normales!
{% endhint %}

¡Y eso es todo! Has actualizado exitosamente ROX a FEG y lo has transferido a otra cadena en solo unos pocos clics. Es simple y fácil.

### Direcciones antiguas de ROX

```
ROX on BSC // 0xa3D522c151aD654b36BDFe7a69D0c405193A22F9
```

```
ROX on ETH // 0x378c77C5379cA07BBB5B3506c08a1C769dEC91c2
```

## FAQ

### ¿Las reclamaciones son automáticas o manuales?

Son manuales, y necesitas usar la herramienta de actualización en [SmartDeFi.com](https://smartdefi.com) para reclamar tus FEG.

### ¿Cómo recibo FEG?

En cada reclamación, tienes 3 opciones para elegir dónde recibir los nuevos FEG:

1. reclamar FEG en una cartera en la cadena actual
2. reclamar FEG en una cartera en la cadena de tu elección (BSC/ETH/BASE)
3. reclamar y apostar automáticamente en la cadena actual

### ¿Cómo se calculó la proporción de ROX y FEG?

Establecimos la proporción utilizando los precios de apertura de FEG y ROX el 15 de mayo de 2022. El valor de ROX y FEG se calculó dividiendo el número de monedas nativas (ETH o BNB) pagadas por el número de tokens (FEG o ROX) recibidos. Para determinar cuánto FEG produce un ROX, dividimos el valor de la moneda nativa de un ROX por el valor de la moneda nativa de un FEG. En términos simples, esta proporción representa la cantidad de FEG que podrías haber comprado por el mismo precio que un ROX.

Transacciones abiertas en BSC\
**ROX**: 0x1a0e998a173ef8b395513f85a44b5abd8db2c9f7a79daf19f477165015843504\
**FEG**: 0x190b55b45916e4c79a98d061d2edd16c8cf67f119fa3544e0273e6f6b6ee1cd0

Transacciones abiertas en ETH\
**ROX** 0x883c756fe5be2182b5e45f80286f8d4c7e2eea23eebe1e15ea53d66932aee026\
**FEG**: 0x0f58396870514f4419ed542dfada345b299971a43f186f1bfc6ea8d29c838bd5\
\* Nota: El 15 de mayo, SOLO se usó una transacción ROX en ETH como precio de apertura.

### ¿Por qué usar valores pre-exploit en lugar de post-exploit para FEG?

Usar variables pre-exploit para ambos tokens se consideró el enfoque más lógico, esencialmente creando una 'instantánea' de las condiciones del mercado antes de que ocurriera cualquier exploit. Mientras que ROX habría enfrentado las mismas condiciones de mercado que FEG post-exploit, evitamos especular sobre el precio y la oferta circulante. En lugar de eso, confiamos en datos crudos de la blockchain en lugar de cifras arbitrarias.

### ¿Por qué no usar los pools de liquidez de ROX y FEG para determinar la proporción?

Elegimos no usar este método por dos razones principales:

1\.   FEG no tenía un LP respaldado por activos como ROX. Mientras que ROX se beneficiaba de tener tanto un LP respaldado por activos como un LP de mercado, FEG solo tenía un LP de mercado. Por lo tanto, usar los LP para determinar la proporción habría sido injusto, ya que FEG no pudo aprovechar la misma tecnología de respaldo de activos que beneficiaba a ROX.

2\.   Para evitar diluir en gran medida a los inversores de FEG, consideramos el LP total para ambos tokens. El LP para ROX BSC era aproximadamente 2.23 veces mayor que el de FEG BSC, y el LP para FEG ETH era aproximadamente 1.42 veces mayor que el de ROX ETH. Usando estas métricas, los poseedores de ROX BSC habrían poseído el 69% de la nueva oferta de FEG V2, y los poseedores de ROX ETH habrían poseído el 41%. Tal discrepancia significativa en la propiedad entre las cadenas habría sido injusta para los poseedores de FEG y podría haber puesto el proyecto en riesgo.

·         LPs de BSC → ROX = 5672 BNB; FEG = 2544 BNB

·         LPs de ETH → ROX = 425 ETH; FEG = 604 ETH