Act 1 creada por Manuel Jesús y José Fernández.

Eligiremos la web de Instagram.

**1. Auditoria de Red(Network):** 

DOC(HTML): 206,5 kB
<img width="1917" height="870" alt="Captura de pantalla 2026-09-22 123204" src="https://github.com/user-attachments/assets/9c185142-4031-4be2-97c0-81e02bea15b1" />

Script de JavaScript:3228 kB
<img width="1666" height="852" alt="Captura de pantalla 2026-09-22 132131" src="https://github.com/user-attachments/assets/70214772-8582-4b03-a137-674871cfcd88" />

La ejecución en el servidor permite que el cliente reciba el HTML completamente procesado y renderizado, lo que ofrece mayor seguridad, un control más estricto sobre los datos y los usuarios, y garantiza una comunicación continua y fiable con el servidor.

**2. Performance** 

* parsing HTML: que se representa como htmlstar y htmlflush
<img width="1670" height="846" alt="Captura de pantalla 2026-09-22 125703" src="https://github.com/user-attachments/assets/3c6d159f-f575-4280-a484-5d0e8851ffcc" />

htmlstar es el inicio en el que Chrome empieza a parsear el HTML recibido del servidor y el htmlflush es cuando termina de procesar un bloque de HTML.

Esto se consigue al iniciar la grabación y a la vez recargar la página.

* Evaluate script: es código ejecutado de JS ejecutado en memoria.
<img width="1666" height="853" alt="Captura de pantalla 2026-09-22 125017" src="https://github.com/user-attachments/assets/b5075416-5b34-4324-8ec8-bc33a3688637" />

* Compile code: barras amarillas finas dentro de esos bloques + sub‑eventos en la tabla inferior.
<img width="1377" height="371" alt="Captura de pantalla 2026-09-22 133135" src="https://github.com/user-attachments/assets/bb1a7427-9e3a-432b-95c3-2bb9457cb759" />

El motor JS ejecuta y procesa codigo de Instagram.

**3. Consola**
   
Creamos la variable "a" que contiene un string y luego un console.log(a) para imprimir por pantalla la variable a.
<img width="747" height="146" alt="Captura de pantalla 2026-09-22 141510" src="https://github.com/user-attachments/assets/06ecaf4b-6985-4235-9245-7c5761616b18" />

Luego con un comando maligno como el Filereader:

<img width="932" height="102" alt="Captura de pantalla 2026-09-22 142630" src="https://github.com/user-attachments/assets/b41e9699-3890-47db-9140-58cd0ec361b2" />

Este error es exactamente lo que debe ocurrir: el navegador está bloqueando el intento de acceder a un archivo del disco usando una ruta local. Es importante para evitar la vulnerabilidad crítica, sin este bloqueo, cualquier página web podría leer tus documentos personales. 

**4. Análisis de bloqueo**

Si un script de 1MB se ejecuta de forma síncrona, la página se congela, pierde fluidez y incluso cerrar el navegador. El modelo asíncrono y orientado a eventos de scripting web evita este bloqueo y mantiene la interfaz reactiva.

