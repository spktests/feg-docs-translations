# ⚙️ Proceso SDR

#### No es un paseo por el parque

El proceso de recuperación es meticuloso, involucrando una secuencia de envolver y desenvolver, convirtiendo tokens en sus formas envueltas y de nuevo a las originales. Lo hemos visto a través de múltiples ciclos, adaptándolo a las necesidades únicas de la configuración de cada proyecto.

#### Liquidez en fBNB y fETH: Envolver y Desenvolver Durante el Proceso de Recuperación

En la primera iteración de SmartDeFi, los proyectos tienen liquidez en fBNB (Binance Coin envuelto) o fETH (Ethereum envuelto).

El proceso de recuperación para estos proyectos conlleva una secuencia meticulosa de envolver y desenvolver, que incluye:

1. **Envolver**: Este proceso implica convertir BNB o ETH en sus formas envueltas (fBNB o fETH).
2. **Desenvolver**: Los tokens envueltos (fBNB o fETH) se convierten de nuevo a sus formas originales (BNB o ETH).
3. **Múltiples Ciclos**: El proceso puede requerir varios ciclos de envolver y desenvolver, adaptándose a las necesidades específicas de cada proyecto y del ecosistema en general.

**Aspectos Adicionales del Proceso de Recuperación**

* **Comisión de Flashloan por PancakeSwap (PCS)**: Es importante tener en cuenta que PancakeSwap cobra y mantiene una comisión por el flashloan, que no es retornable como parte del proceso de recuperación.
* **Variabilidad de la Tarifa:** El costo incurrido varía entre el 22% y el 28%, incluyendo los impuestos fWrap incurridos durante el proceso de envolver y desenvolver, distribuidos como reflejos. El costo puede aumentar si es necesario realizar una re-recuperación (múltiples intentos debido al tamaño del pool de liquidez).
* **Decisión de Enrutamiento para Flashloans**: Se tomó una decisión estratégica de enrutar los flashloans a través de nuestro pool FEG/BNB en lugar de optar por uno de los pools de PancakeSwap, como BNB/USDT. Esta elección asegura que las tarifas impuestas por PancakeSwap se asignen en parte a nuestro pool de liquidez (LP) de FEG en lugar de ser dirigidas completamente a PancakeSwap. Notablemente, ejecutar un flashloan requiere aproximadamente 4.5 veces más BNB que la liquidez en el pool que se recupera. Consecuentemente, a medida que el proceso de recuperación avanza, puede haber un aumento notable en la liquidez total de FEG y BNB en nuestro pool, lo cual es un resultado directo de estas decisiones de enrutamiento.
* **Asignación de Tarifas**: PancakeSwap añade la parte parcialmente recolectada de la comisión a un pool preasignado de Tokens FEG a una proporción de dólar igual al pool de liquidez, pero no emite tokens LP por esta comisión. En cambio, debemos proporcionar Tokens FEG para igualar la comisión parcial. Esta cantidad igualada se coloca luego en el pool de liquidez FEG.

Nuestro equipo está comprometido con la gestión de estas complejidades para asegurar la recuperación eficiente de proyectos mientras se mantiene la estabilidad y vitalidad de nuestro ecosistema. Valoramos su apoyo continuo y estamos dedicados a la transparencia mientras navegamos por este intrincado proceso de recuperación.