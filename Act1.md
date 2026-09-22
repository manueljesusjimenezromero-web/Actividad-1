<img width="1726" height="797" alt="Captura de pantalla 2026-09-22 123223" src="https://github.com/user-attachments/assets/7b766e71-1177-4fd8-b88e-9a81f6df4107" />

# Acto 1 — Auditoría técnica de Instagram Web  
**Autores:** Manuel Jesús y José Fernández

---

## 1. Auditoría de Red (Network)

### 📄 Documento HTML (DOC)
**Tamaño:** 206,5 kB

Instagram entrega un HTML ya procesado desde el servidor, lo que indica uso de **renderizado del lado del servidor (SSR)**.  
Esto permite:
- Mayor velocidad en la carga inicial.  
- Más seguridad y control sobre los datos del usuario.  
- Comunicación constante con el servidor.
<img width="1917" height="870" alt="Captura de pantalla 2026-09-22 123204" src="https://github.com/user-attachments/assets/f3a36293-b6e5-491a-9127-35cb07a611bd" />
---

### 📜 Scripts de JavaScript
**Tamaño total:** 3228 kB

Instagram divide su JavaScript en múltiples bundles ofuscados. Estos scripts contienen:
- React y su sistema de renderizado.  
- Lógica interna de la aplicación.  
- Módulos cargados dinámicamente.  
- Código para animaciones, reproducción de reels y eventos.  

El navegador descarga estos archivos y el motor JS los ejecuta para generar la experiencia interactiva.

---

## 2. Performance (Rendimiento)

La grabación de rendimiento muestra cómo el navegador procesa el HTML y ejecuta el JavaScript de Instagram.

---

### 🔹 Parsing HTML (htmlstar y htmlflush)

- **htmlstar** → Inicio del parseo del HTML recibido del servidor.  
- **htmlflush** → Finalización del procesamiento de un bloque de HTML.

Estos eventos aparecen al **iniciar la grabación y recargar la página**.

---

### 🔹 Evaluate Script

**Evaluate script** representa **código JavaScript ejecutado directamente en memoria**, no descargado como archivo independiente.

Instagram genera gran parte de su lógica de forma dinámica, por lo que el motor JS ejecuta:
- Código inline.  
- Funciones creadas por React.  
- Módulos cargados bajo demanda.  
- Callbacks del reproductor de reels.

Por eso este evento **no tiene tamaño** en la pestaña Network.

---

### 🔹 Compile Code

Las barras amarillas finas dentro de los bloques de ejecución representan **Compile code**, es decir:
- Trabajo del motor JS preparando funciones para ejecutarse.  
- Optimización interna del código.  
- Sub‑eventos visibles en la tabla inferior (*Bottom‑Up*).

Esto ocurre constantemente en aplicaciones complejas como Instagram.

---

## 3. Qué está haciendo el motor JavaScript

El motor JS está realizando todas las tareas necesarias para que Instagram funcione de forma fluida:

- Ejecutar funciones del bundle (React + módulos internos).  
- Actualizar la interfaz mediante commits de React.  
- Procesar animaciones del reel con `requestAnimationFrame`.  
- Programar tareas diferidas con `setTimeout`.  
- Gestionar eventos del usuario y del reproductor de vídeo.  
- Optimizar y compilar código dinámico.

---

### 🟩 Resumen

**El motor JavaScript interpreta, ejecuta y optimiza el código de Instagram para renderizar la interfaz, reproducir el reel y mantener la aplicación interactiva.**

