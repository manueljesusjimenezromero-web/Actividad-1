
**Experimento de integracion**:

Escenario A:

<img width="787" height="402" alt="Captura de pantalla 2026-09-24 090248" src="https://github.com/user-attachments/assets/e3e0b9e8-f01d-4929-9ea4-db8f0ab11fe1" />

Escenario B

<img width="617" height="372" alt="Captura de pantalla 2026-09-25 100508" src="https://github.com/user-attachments/assets/da821851-0816-4f12-9098-2aa7177bb48b" />

Escenario C

<img width="617" height="376" alt="Captura de pantalla 2026-09-24 091338" src="https://github.com/user-attachments/assets/82120761-cf2d-416f-a23f-48a221261598" />

Escenario D

<img width="651" height="387" alt="Captura de pantalla 2026-09-24 091535" src="https://github.com/user-attachments/assets/a13f04a0-d7ab-46ea-b318-6803af724478" />

Escenario E

<img width="662" height="392" alt="Captura de pantalla 2026-09-24 092305" src="https://github.com/user-attachments/assets/3b841bae-5b89-413c-bf1b-b6c45eb170c3" />

**Informe de Resultados**

**Escenario A**

Tarda 5,085 ms.

En este escenario, bloquea el parseo, haciendo que la página no se vea hasta que los scripts terminen. Esto provoca un mal rendimiento, pero garantiza un orden de ejecución.

<img width="1337" height="912" alt="Captura de pantalla 2026-09-25 121148" src="https://github.com/user-attachments/assets/ae9aad52-5401-4afc-a275-b3bfed8776cd" />

<img width="1326" height="917" alt="Captura de pantalla 2026-09-25 121233" src="https://github.com/user-attachments/assets/7abffc85-8de8-4fc1-a501-626d8a9802c0" />


**Escenario B**

Tarda 5,058 ms.

No bloquea el parseo, permite ver el contenido rápidamente y los scripts se ejecutan después del DOM, pero antes del evento, con un orden de ejecución.

<img width="1342" height="917" alt="Captura de pantalla 2026-09-25 120803" src="https://github.com/user-attachments/assets/c4028a13-a23c-4801-a850-2f38be3c311a" />

<img width="1337" height="877" alt="Captura de pantalla 2026-09-25 120837" src="https://github.com/user-attachments/assets/f53a28cf-1141-4cb0-be0e-b0cb0ff51410" />


**Escenario C**

Tarda 5,089 ms.

No bloquea el parseo, permite ver el contenido rápidamente y los scripts se ejecutan después del DOM, pero antes del evento, con un orden de ejecución. También provoca un mal rendimiento.

<img width="1346" height="927" alt="Captura de pantalla 2026-09-25 120501" src="https://github.com/user-attachments/assets/f26c4a0f-31bd-40de-897a-e56b890eeeb9" />

<img width="1317" height="917" alt="Captura de pantalla 2026-09-25 120622" src="https://github.com/user-attachments/assets/99d44fc5-a747-4820-8718-54622d4d44e0" />

**Escenario D**

Tarda 5,098 ms.

El navegador analiza todo el HTML, construye el DOM completo, ejecución de scripts en orden.

<img width="1316" height="892" alt="Captura de pantalla 2026-09-25 115659" src="https://github.com/user-attachments/assets/beda8c28-74a6-4a65-8718-776d512f8d81" />

<img width="1332" height="836" alt="Captura de pantalla 2026-09-25 115957" src="https://github.com/user-attachments/assets/bc4d93eb-e673-42c3-95bd-bc7d61a195a4" />


**Escenario E**

Tarda 5,063

Comportamiento parecido al de defer: retrasa la ejecución hasta que termine el parseo. El DOM ya está construido cuando normalmente se ejecuta.

<img width="1327" height="875" alt="Captura de pantalla 2026-09-25 120248" src="https://github.com/user-attachments/assets/3eca0263-5af5-4222-bcfc-90b42fd8b251" />

<img width="1331" height="912" alt="Captura de pantalla 2026-09-25 120328" src="https://github.com/user-attachments/assets/5636313e-067a-48ea-9596-bc4e8a656871" />

