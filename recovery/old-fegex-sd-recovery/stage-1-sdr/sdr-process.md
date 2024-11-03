# ⚙️ Proceso SDR

#### No es un paseo por el parque

El proceso de recuperación es meticuloso, involucrando una secuencia de envolver y desenvolver, convirtiendo tokens en sus formas envueltas y viceversa. Lo hemos visto a través de múltiples ciclos, adaptándolo a las necesidades únicas de la configuración de cada proyecto.

#### Liquidez en fBNB y fETH: Envolver y Desenvolver Durante el Proceso de Recuperación

En la primera iteración de SmartDeFi, los proyectos tienen liquidez en fBNB (Binance Coin envuelto) o fETH (Ethereum envuelto).

El proceso de recuperación para estos proyectos implica una secuencia meticulosa de envolver y desenvolver, que incluye:

1. **Envolver**: Este proceso implica convertir BNB o ETH en sus formas envueltas (fBNB o fETH).
2. **Desenvolver**: Los tokens envueltos (fBNB o fETH) se convierten de nuevo a sus formas originales (BNB o ETH).
3. **Múltiples Ciclos**: El proceso puede requerir varios ciclos de envolver y desenvolver, adaptados a las necesidades específicas de cada proyecto y del ecosistema en general.

**Aspectos Adicionales del Proceso de Recuperación**

* **Tarifa de Préstamo Relámpago por PancakeSwap (PCS)**: Es importante notar que PancakeSwap cobra y retiene una tarifa por el préstamo relámpago, que no es retornable como parte del proceso de recuperación.
* **Variabilidad de Tarifas**: El costo incurrido varía del 22% al 28%, incluyendo los impuestos fWrap incurridos durante el proceso de envolver y desenvolver, distribuidos como reflexiones. El costo puede aumentar si es necesaria una re-recuperación (múltiples intentos debido al tamaño del pool de liquidez).
* **Decisión de Enrutamiento para Préstamos Relámpago**: Se tomó una decisión estratégica de enrutar los préstamos relámpago a través de nuestro pool FEG/BNB en lugar de optar por uno de los pools de PancakeSwap, como BNB/USDT. Esta elección asegura que las tarifas impuestas por PancakeSwap se asignen en parte a nuestro pool de liquidez de FEG (LP) en lugar de ser dirigidas completamente a PancakeSwap. Notablemente, ejecutar un préstamo relámpago requiere aproximadamente 4.5 veces más BNB que la liquidez en el pool que se está recuperando. En consecuencia, a medida que progresa el proceso de recuperación, puede haber un aumento notable en la liquidez total de FEG y BNB en nuestro pool, lo cual es un resultado directo de estas decisiones de enrutamiento.
* **Asignación de Tarifas**: PancakeSwap añade la tarifa parcialmente recolectada a un pool preasignado de Tokens FEG en una relación de valor en dólares igual al pool de liquidez, pero no emite tokens LP por esta tarifa. En cambio, debemos proporcionar Tokens FEG para igualar la tarifa parcial. Esta cantidad igualada se coloca en el pool de liquidez FEG.

Nuestro equipo está comprometido a gestionar estas complejidades para asegurar la eficiente recuperación de proyectos mientras mantenemos la estabilidad y vitalidad de nuestro ecosistema. Valoramos su apoyo continuo y estamos dedicados a la transparencia mientras navegamos este intrincado proceso de recuperación.