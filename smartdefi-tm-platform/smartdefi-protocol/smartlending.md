---
description: Préstamos sin intereses hechos simples.
---

# 🏦 SmartLending

<figure><img src="../../.gitbook/assets/Screenshot_17.png" alt=""><figcaption></figcaption></figure>

A través de _SmartLending_, cualquier token SmartDeFi puede utilizarse como garantía para obtener préstamos contra su valor base, sin necesidad de vender o quemar el Token.

Al tomar el préstamo, el prestatario recibe instantáneamente el valor base del Token garantizado. El prestatario luego tiene **30 días** para reembolsar el préstamo _sin intereses_.\
\
Si el préstamo no puede ser reembolsado a tiempo, el usuario puede extender el período de préstamo por otros 30 días quemando el 0.1% de su garantía, y puede extenderse una y otra vez.

{% hint style="warning" %}
Nota: Extender SmartLoan antes de la expiración de los 30 días es esencial. De lo contrario, el préstamo entra en incumplimiento y la garantía se quema (se pierde).
{% endhint %}

{% hint style="success" %}
Debido a que los tokens garantizados se mantienen dentro del contrato inteligente y se consideran parte del suministro circulante, continúan acumulando respaldo de activos como lo harían en la billetera del inversor. La continua acumulación de respaldo de activos permite que SmartLending sea _sin intereses._&#x20;
{% endhint %}

### ¿Qué significa esto?

SmartLending significa que ahora puedes acceder al valor base de tu token SmartDeFi sin venderlo. Esto es perfecto para emergencias o para aprovechar el lanzamiento de un nuevo Token sin vender tus activos.\
\
Esto significa que tienes libertad y puedes tratar tu valor base como un activo bancarizado.

### ¿Qué tan seguro es?

SmartLend no requiere oráculos, ya que el precio proviene directamente del valor base extraído del contrato inteligente. Además, como SmartLend no requiere tercero, no hay lugar para manipulaciones externas o explotaciones del código.

{% hint style="success" %}
**SmartLend es el primer protocolo de préstamo en el cual los fondos y los datos para los cálculos de proporción se alojan en el mismo lugar, haciéndolo el protocolo más seguro jamás creado.**
{% endhint %}

### ¿Hay un impuesto por prestar un Token SmartDeFi?

No, pero si un Token SmartDeFi ™ tiene un impuesto de reflexión, prestar contra él CAUSARÁ que ese impuesto de reflexión sea deducido.

### ¿Por qué el Token no aparece en la billetera después de tomar un préstamo?

SmartLend retiene el Token del usuario en el Contrato Inteligente como garantía mientras otorga el tipo de token de respaldo del activo al valor base del Token. Por ejemplo, si el Token está respaldado por activos en wBNB, el préstamo se proporcionará en wBNB.

### ¿Los Tokens dentro de SmartLend reciben reflexiones (RFI)?

**No**, no las reciben. Una vez que un Token se utiliza como garantía para un préstamo SmartLend, los tokens SD no reciben reflexiones mientras están retenidos dentro del Contrato Inteligente.

### ¿Puedo reembolsar en partes?

Puedes reembolsar en tantas partes como desees, y también recibirás tu token SD en partes.\
Una vez que un usuario reembolsa la parte final y, por lo tanto, reembolsa su préstamo por completo, todos los Tokens SD restantes se devuelven al usuario en su billetera, y los tokens SD comenzarán nuevamente a recibir reflexiones si el Token es reflectante (RFI).