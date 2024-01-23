---
Author: Coderhouse
Category: Fundamentos de Data
Type: Apunte
Status: Terminado
relación: "[[fundamentos de Ingenieria de datos]]"
---
# Online Transaction processing 

Estos se enfocan en la Escritura de transacciones y lectura de datos específicos. 

### Ejemplo
Sistema bancario: Clientes, cuentas bancarias y transacciones de dinero.
- Se crea una nueva cuenta - Escritura
- Que un usuario envié dinero a otro usuario - Escritura
- Que paguen productos con la cuenta bancaria - Escritura
- Leer el balance de lo que le queda.- Lectura

Se suelen usar mucho los
- [[INSERT]]
- [[UPDATE]]
- [[DELETE]]
- Pocos [[SELECT]] para ver cosas especificas. 
Es información que sirve mas para que los usuarios puedan ver esa información.

Estas [[Base de datos]] Son muy [[Normalización|Normalizadas]] y no almacenan [[Datos]] analiticos y tampoco datos históricos.