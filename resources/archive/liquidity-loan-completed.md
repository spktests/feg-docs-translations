# 💼 Préstamo de Liquidez \[Completado]

## Total de Repago = 100% Reembolsado (16 de octubre de 2024).

### El 13 de marzo de 2023, FEG aseguró un préstamo de 200 ETH convertido en BNB para reponer el fondo de liquidez FEGbsc para el nuevo contrato de token después de la migración.

## Detalles del Préstamo:

* Este préstamo se pagará como 200 ETH (La forma en que fue otorgado).
* Se pagará una tarifa fija de $50,000 USD en interés al proveedor de LP.

## Contrato de Repago del Préstamo:

El equipo de FEG (Feed Every Gorilla) ha establecido un nuevo contrato, definiendo un plan para asignar el 50% de la liquidez de FEG, abarcando tanto tokens FEGeth como FEGbsc. Según este acuerdo, el prestamista proveedor de liquidez (LP) puede reclamar una parte de esta liquidez quincenalmente.

**Características Clave del Contrato:**

1. **Reclamaciones Quincenales:** El prestamista LP está autorizado a reclamar hasta el 10% de la liquidez del 50% asignado cada dos semanas de cada cadena (FEGeth & FEGbsc).\
   \- Nota: El BNB retirado de la liquidez FEGbsc será convertido a ETH para mantener un conteo de repago preciso.
2. **Gestión Estratégica de Liquidez:** Este proceso de reclamo gradual está diseñado para proporcionar suficiente tiempo para que el precio del token FEG potencialmente aumente. El objetivo es usar menos del 50% total asignado, con la liquidez restante siendo eventualmente devuelta al fondo de liquidez de FEG, preservando y estabilizando así la liquidez general.

## Implementación del Contrato LP

El contrato LP ha sido completamente auditado y probado. Los desarrolladores de FEG han implementado exitosamente el contrato y transferido una porción del LP al mismo, como se evidencia en las siguientes transacciones:\
\
\- LP de FEGbsc movido al Contrato de Préstamo:

Contrato 1

https://bscscan.com/tx/0xbcd70a4e92518d83646fcd58753a76ddb0f8c333d4f6bd5400cd9697f6f676cc

Contrato 2

https://bscscan.com/tx/0x970b49dedcefbd8e8f194bd3223c4572401c2d02a61c6322a4f977edbb3b24d0&#x20;

\
\- LP de FEGeth movido al Contrato de Préstamo:

https://etherscan.io/tx/0x0c7a7916a0c12460dec959415d87ad273855c164e0149af8a5088cf1228ad976

***

## Transacciones de Pago de Intereses

3 de abril de 2024

25,000$

https://etherscan.io/tx/0x33fa125ac18283d9d7d6ff39070b106d753a4467a30889bfb04551baa864833a

https://bscscan.com/tx/0xfefb48093e81c7de21285f93b839f46155ef30bbbf5a1244695c9709c6812689

https://bscscan.com/tx/0x7898a88b172511079401bae4a94a25c69cc9a525d0df1007c882da5b7cd6a3d0

## **Abordando la Disminución de Liquidez: Solución de "Vinculación" de Liquidez**

En respuesta a la posible disminución de la liquidez debido a estos retiros, FEGrox ha desarrollado un innovador contrato de "vinculación". Este contrato permite a los usuarios contribuir con ETH o BNB, que se emparejarán con los Tokens FEG no pareados tras los retiros de liquidez por parte del prestamista.

**Detalles del Contrato de Vinculación:**

* **Duración:** Los bonos tendrán un plazo de un año.
* **Retorno del Bono:** Al final de este período, los usuarios recibirán de vuelta su ETH o BNB "vinculados", junto con la cantidad equivalente de tokens FEG que contribuyeron al par.
* **Conciencia de Riesgo:** Los participantes deben ser conscientes de la posibilidad de pérdida impermanente, un riesgo común para todos los proveedores de liquidez.

El contrato de "vinculación" representa un enfoque estratégico para fortalecer el fondo de liquidez y mitigar los efectos del retiro de liquidez por parte del prestamista. Este enfoque no solo ayuda a mantener un nivel de liquidez saludable sino que permite a los usuarios contribuir y beneficiarse del ecosistema FEG.

Más información sobre este mecanismo de "vinculación" será liberada a su debido tiempo, incluyendo detalles sobre su prueba y auditoría. Esta medida proactiva demuestra el compromiso de FEG de mantener una liquidez robusta y un ecosistema estable para sus usuarios e inversores.

***

## Tokenomics

[Tokenomics](../../feg-smartdefi-tm/about-feg-token/feg-tokenomics.md) fueron ajustados para satisfacer las necesidades del proyecto, incluyendo el aumento del impuesto total para incorporar un impuesto de Inyección de Liquidez que ayudaría a estabilizar la liquidez durante el repago del préstamo.

***

## Transacciones de Préstamo de ETH & Conversión de ETH a BNB

|                                                                                200 ETH enviados por el Prestamista                                                                                |                                                                                 Conversiones de ETH a BNB                                                                                 |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [https://bscscan.com/tx/0x8ad053c6ced51d6a02ab253e49de1c32637090e0bba8076552fc91c4090826fb](https://bscscan.com/tx/0x8ad053c6ced51d6a02ab253e49de1c32637090e0bba8076552fc91c4090826fb) | [https://bscscan.com/tx/0xebb747ffeebdf4f498bd8d0585b6c66f9da9f68f9d58ecf2fac6a8a83aec3a7c](https://bscscan.com/tx/0xebb747ffeebdf4f498bd8d0585b6c66f9da9f68f9d58ecf2fac6a8a83aec3a7c) |
| [https://bscscan.com/tx/0x0ba3162a4b4096d86e37af4c128ecf54d9dd43504fcb5b5d7bc316f9b938e964](https://bscscan.com/tx/0x0ba3162a4b4096d86e37af4c128ecf54d9dd43504fcb5b5d7bc316f9b938e964) | [https://bscscan.com/tx/0xd0f0d3ffea907594f29e1f3e03a7d0c212faf65521e92ab623f60da9d0e8516d](https://bscscan.com/tx/0xd0f0d3ffea907594f29e1f3e03a7d0c212faf65521e92ab623f60da9d0e8516d) |
| [https://bscscan.com/tx/0x6a1d461e5b472ee10790ddc53127daca73a46013ea4dfae7b0a2a828bb5370c1](https://bscscan.com/tx/0x6a1d461e5b472ee10790ddc53127daca73a46013ea4dfae7b0a2a828bb5370c1) | [https://bscscan.com/tx/0xb4c6a34096ddfac65dfd585f6ef91cdb65d8a128b22106be8a10a605b92dc351](https://bscscan.com/tx/0xb4c6a34096ddfac65dfd585f6ef91cdb65d8a128b22106be8a10a605b92dc351) |
| [https://bscscan.com/tx/0x3dcb86988985690beea21605ece7deec3ffc71a1eccbdf1cab5a1a6ef08cef00](https://bscscan.com/tx/0x3dcb86988985690beea21605ece7deec3ffc71a1eccbdf1cab5a1a6ef08cef00) | [https://bscscan.com/tx/0x9386d633161551c3a59942feaab9c7d00aae7a0770a05bd40ec35682a58aa489](https://bscscan.com/tx/0x9386d633161551c3a59942feaab9c7d00aae7a0770a05bd40ec35682a58aa489) |
| [https://bscscan.com/tx/0x909d5fbbeb5dacceaddc505611dd770e8ee3faf6384f97248cc1b2df5484e0b1](https://bscscan.com/tx/0x909d5fbbeb5dacceaddc505611dd770e8ee3faf6384f97248cc1b2df5484e0b1) | [https://bscscan.com/tx/0x3bb7e146c824775c32f323921fdfeffc9b4b6941914aa3c186c0f47fbcd2e366](https://bscscan.com/tx/0x3bb7e146c824775c32f323921fdfeffc9b4b6941914aa3c186c0f47fbcd2e366) |
|                                                                                                                                                                                        | [https://bscscan.com/tx/0xb1abab7d58c29b9e9ef491f9839e74b6bfb5aba636bac25d4e468cfa29d732e6](https://bscscan.com/tx/0xb1abab7d58c29b9e9ef491f9839e74b6bfb5aba636bac25d4e468cfa29d732e6) |
|                                                                                                                                                                                        | [https://bscscan.com/tx/0x6369aaff0a8482c1c561aa4778fc927857cfa4498dd685703609f6a3a7f122ee](https://bscscan.com/tx/0x6369aaff0a8482c1c561aa4778fc927857cfa4498dd685703609f6a3a7f122ee) |

***

## Cómo calcular Inyecciones de Liquidez impulsadas por la Tokenomics

Hicimos que el usuario pueda ver en la blockchain y observar los fondos almacenados; como tal, los fondos reunidos por los impuestos para el repago del préstamo se mantienen directamente dentro del contrato del token.\
Los fondos se almacenan dentro del contrato de FEG como tokens LP.\
\
**Dirección del Contrato BSC LP**:\
[https://bscscan.com/address/0xF53a1d602281B1ce2A92A1763364d2981269a72C](https://bscscan.com/address/0xF53a1d602281B1ce2A92A1763364d2981269a72C)\
**Dirección del Contrato ETH LP**:\
[https://etherscan.io/address/0x60EF1e0Bf9218Cdc1769a43c4B0B111ed38BB418](https://etherscan.io/address/0x60EF1e0Bf9218Cdc1769a43c4B0B111ed38BB418)\
\
Para calcular cuánto BNB/ETH se ha reunido dentro de esos tokens LP:\
1\. Presiona el botón desplegable del token para ver el total de BNB o ETH en el contrato LP\
2\. Haz clic en Pancake LP (BSC) o Uniswap V2 (ETH) bajo "Token Tracker".\
3\. Haz clic en la pestaña "Holders"\
4\. Localiza la dirección del contrato FEG (`0xbededDf2eF49E87037c4fb2cA34d1FF3D3992A11`) que debería ser la cartera #2\
5\. Desplázate a la derecha y nota el porcentaje que la cartera #2 (contrato FEG) tiene\
6\. Multiplica ese porcentaje por el total de BNB o ETH en el contrato LP para encontrar cuánto se ha generado para el repago del préstamo.

<figure><img src="../../.gitbook/assets/Screenshot_8 (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot_9 (1).png" alt=""><figcaption></figcaption></figure>

***

## Transacciones de Repago del Préstamo (antes de la creación del contrato)

El primer repago de 20 ETH se realizó el 8 de mayo de 2023.\
Los detalles son los siguientes:&#x20;

{% code overflow="wrap" %}
```
12 wETH (ERC-20)
https://etherscan.io/tx/0xd9ed4d7c807a6b4a5ec5a24a4e9ce86bf08933a5c914d18c4765272c87396615

8 wETH (BEP-20)
https://bscscan.com/tx/0x559a180c15bde77651cb0dc6124201f735c76122a9970eb266da1174860a0139


📃Liquidity Removal Transactions:

ETH:
Removal from FEG contract:
https://etherscan.io/tx/0x52a52b5991450df3055b561af1c224601fc807f8cf4b11cfb7b44c350f3bdd00

Removal from Uniswap:
https://etherscan.io/tx/0x0a91ad950c81d6b576a6d5c89b6c9d22b7fe5a5f7cdd81e36a10e2a769ca6722

BSC:
Removal from FEG contract:
https://bscscan.com/tx/0xcec80058ac478d7742614b799a353fcbfb840c7653009df51f16442b97713064

Removal from PancakeSwap:
https://bscscan.com/tx/0x2958802bc5897da99ac5638fcf5c480e50ce79ee127f55995ab8ab564fbb5a12

```
{% endcode %}