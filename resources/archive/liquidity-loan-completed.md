# 💼 Préstamo de Liquidez \[Completado]

## Total de Reembolso = 100% Reembolsado (16 de octubre de 2024).

### El 13 de marzo de 2023, FEG aseguró un préstamo de 200 ETH convertido en BNB para reponer el pool de liquidez FEGbsc para el nuevo contrato de token posterior a la migración.

## Detalles del Préstamo:

* Este préstamo se reembolsará como 200 ETH (en la forma en que se otorgó).
* Se pagará una tarifa fija de intereses de $50,000 USD al proveedor de LP.

## Contrato de Reembolso del Préstamo:

El equipo de FEG (Feed Every Gorilla) ha establecido un nuevo contrato, configurando un plan para asignar el 50% de la liquidez de FEG, incluyendo tanto los tokens FEGeth como FEGbsc. Bajo este acuerdo, el prestamista del proveedor de liquidez (LP) puede reclamar una porción de esta liquidez quincenalmente.

**Características Clave del Contrato:**

1. **Reclamaciones Quincenales:** El prestamista LP está autorizado a reclamar hasta el 10% de la liquidez asignada del 50% cada dos semanas de cada cadena (FEGeth & FEGbsc).\
   \- Nota: El BNB retirado de la liquidez FEGbsc se convertirá en ETH para mantener un conteo de reembolso preciso.
2. **Gestión Estratégica de Liquidez:** Este proceso de reclamación escalonado está diseñado para proporcionar tiempo suficiente para que el precio del token FEG pueda aumentar. El objetivo es usar menos del 50% total asignado, con la liquidez restante eventualmente regresando al pool de liquidez FEG, preservando y estabilizando la liquidez general.

## Contrato LP Implementado

El contrato de LP ha sido completamente auditado y probado. Los desarrolladores de FEG han implementado con éxito el contrato y transferido una porción del LP a él, como se evidencia en las siguientes transacciones:\
\
\- LP FEGbsc trasladado al Contrato de Préstamo:

Contrato 1

https://bscscan.com/tx/0xbcd70a4e92518d83646fcd58753a76ddb0f8c333d4f6bd5400cd9697f6f676cc

Contrato 2

https://bscscan.com/tx/0x970b49dedcefbd8e8f194bd3223c4572401c2d02a61c6322a4f977edbb3b24d0&#x20;

\
\- LP FEGeth trasladado al Contrato de Préstamo:

https://etherscan.io/tx/0x0c7a7916a0c12460dec959415d87ad273855c164e0149af8a5088cf1228ad976

***

## Transacciones de Reembolso de Intereses

3 de abril de 2024

25,000$

https://etherscan.io/tx/0x33fa125ac18283d9d7d6ff39070b106d753a4467a30889bfb04551baa864833a

https://bscscan.com/tx/0xfefb48093e81c7de21285f93b839f46155ef30bbbf5a1244695c9709c6812689

https://bscscan.com/tx/0x7898a88b172511079401bae4a94a25c69cc9a525d0df1007c882da5b7cd6a3d0

## **Abordando la Reducción de Liquidez: Solución de "Vinculación" de Liquidez**

En respuesta a la posible reducción de la liquidez debido a estos retiros, FEGrox ha desarrollado un innovador contrato de "vinculación". Este contrato permite a los usuarios contribuir con ETH o BNB, que se emparejarán con los Tokens FEG no emparejados tras los retiros de liquidez por parte del prestamista.

**Detalles del Contrato de Vinculación:**

* **Duración:** Los bonos tendrán un plazo de un año.
* **Retorno del Bono:** Al final de este período, los usuarios recibirán de vuelta su ETH o BNB "vinculado", junto con la cantidad equivalente de tokens FEG que contribuyeron al par.
* **Conciencia de Riesgo:** Los participantes deben ser conscientes de la posibilidad de pérdida impermanente, un riesgo común para todos los proveedores de liquidez.

El contrato de "vinculación" representa un enfoque estratégico para fortalecer el pool de liquidez y mitigar los efectos del retiro de liquidez por parte del prestamista. Este enfoque no solo ayuda a mantener un nivel saludable de liquidez, sino que permite a los usuarios contribuir y beneficiarse del ecosistema FEG.

Se publicará más información sobre este mecanismo de "vinculación" a su debido tiempo, incluidos detalles sobre su prueba y auditoría. Esta medida proactiva demuestra el compromiso de FEG con el mantenimiento de una liquidez robusta y un ecosistema estable para sus usuarios e inversionistas.

***

## Tokenómica

[Tokenomics](../../feg-smartdefi-tm/about-feg-token/feg-tokenomics.md) se ajustaron para satisfacer las necesidades del proyecto, incluyendo el aumento del impuesto total para incluir un impuesto de Inyección de Liquidez que ayudaría a estabilizar la liquidez durante el reembolso del préstamo.

***

## Transacciones de Préstamo ETH & Conversión de ETH a BNB

|                                                                                200 ETH enviado por Prestamista                                                                                |                                                                                 Conversión de ETH a BNB                                                                                 |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [https://bscscan.com/tx/0x8ad053c6ced51d6a02ab253e49de1c32637090e0bba8076552fc91c4090826fb](https://bscscan.com/tx/0x8ad053c6ced51d6a02ab253e49de1c32637090e0bba8076552fc91c4090826fb) | [https://bscscan.com/tx/0xebb747ffeebdf4f498bd8d0585b6c66f9da9f68f9d58ecf2fac6a8a83aec3a7c](https://bscscan.com/tx/0xebb747ffeebdf4f498bd8d0585b6c66f9da9f68f9d58ecf2fac6a8a83aec3a7c) |
| [https://bscscan.com/tx/0x0ba3162a4b4096d86e37af4c128ecf54d9dd43504fcb5b5d7bc316f9b938e964](https://bscscan.com/tx/0x0ba3162a4b4096d86e37af4c128ecf54d9dd43504fcb5b5d7bc316f9b938e964) | [https://bscscan.com/tx/0xd0f0d3ffea907594f29e1f3e03a7d0c212faf65521e92ab623f60da9d0e8516d](https://bscscan.com/tx/0xd0f0d3ffea907594f29e1f3e03a7d0c212faf65521e92ab623f60da9d0e8516d) |
| [https://bscscan.com/tx/0x6a1d461e5b472ee10790ddc53127daca73a46013ea4dfae7b0a2a828bb5370c1](https://bscscan.com/tx/0x6a1d461e5b472ee10790ddc53127daca73a46013ea4dfae7b0a2a828bb5370c1) | [https://bscscan.com/tx/0xb4c6a34096ddfac65dfd585f6ef91cdb65d8a128b22106be8a10a605b92dc351](https://bscscan.com/tx/0xb4c6a34096ddfac65dfd585f6ef91cdb65d8a128b22106be8a10a605b92dc351) |
| [https://bscscan.com/tx/0x3dcb86988985690beea21605ece7deec3ffc71a1eccbdf1cab5a1a6ef08cef00](https://bscscan.com/tx/0x3dcb86988985690beea21605ece7deec3ffc71a1eccbdf1cab5a1a6ef08cef00) | [https://bscscan.com/tx/0x9386d633161551c3a59942feaab9c7d00aae7a0770a05bd40ec35682a58aa489](https://bscscan.com/tx/0x9386d633161551c3a59942feaab9c7d00aae7a0770a05bd40ec35682a58aa489) |
| [https://bscscan.com/tx/0x909d5fbbeb5dacceaddc505611dd770e8ee3faf6384f97248cc1b2df5484e0b1](https://bscscan.com/tx/0x909d5fbbeb5dacceaddc505611dd770e8ee3faf6384f97248cc1b2df5484e0b1) | [https://bscscan.com/tx/0x3bb7e146c824775c32f323921fdfeffc9b4b6941914aa3c186c0f47fbcd2e366](https://bscscan.com/tx/0x3bb7e146c824775c32f323921fdfeffc9b4b6941914aa3c186c0f47fbcd2e366) |
|                                                                                                                                                                                        | [https://bscscan.com/tx/0xb1abab7d58c29b9e9ef491f9839e74b6bfb5aba636bac25d4e468cfa29d732e6](https://bscscan.com/tx/0xb1abab7d58c29b9e9ef491f9839e74b6bfb5aba636bac25d4e468cfa29d732e6) |
|                                                                                                                                                                                        | [https://bscscan.com/tx/0x6369aaff0a8482c1c561aa4778fc927857cfa4498dd685703609f6a3a7f122ee](https://bscscan.com/tx/0x6369aaff0a8482c1c561aa4778fc927857cfa4498dd685703609f6a3a7f122ee) |

***

## Cómo calcular las Inyecciones de Liquidez impulsadas por la Tokenómica

Hicimos que el usuario pueda mirar la blockchain y ver los fondos almacenados; por lo tanto, los fondos recaudados por los impuestos para el reembolso del préstamo se mantienen directamente dentro del contrato de token.\
Los fondos se almacenan dentro del contrato de FEG como tokens LP.\
\
**Dirección del Contrato LP BSC:**\
[https://bscscan.com/address/0xF53a1d602281B1ce2A92A1763364d2981269a72C](https://bscscan.com/address/0xF53a1d602281B1ce2A92A1763364d2981269a72C)\
**Dirección del Contrato LP ETH:**