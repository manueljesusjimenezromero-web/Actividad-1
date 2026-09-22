
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

- **htmlstar** → Inicio del
