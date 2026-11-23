# Estudio 4º Dan · Taekwon-Do ITF

App de estudio (teoría, práctica con tarjetas, simulacros y plan). Es un solo `index.html`: funciona sin servidor.
Sin configurar nada, el progreso se guarda en el navegador. Para sincronizarlo entre dispositivos, configurá Firebase (gratis):

## 1. Publicar en GitHub Pages
1. Creá un repositorio nuevo y subí todos estos archivos (incluido `.nojekyll`).
2. Settings → Pages → *Deploy from a branch* → `main` / `/ (root)` → Save.
3. Tu app queda en `https://TU_USUARIO.github.io/NOMBRE_DEL_REPO/`.

## 2. Sincronización con Firebase
1. https://console.firebase.google.com → *Agregar proyecto* (sin Google Analytics).
2. *Compilación → Authentication → Comenzar → Google* → Habilitar → elegí tu mail → Guardar.
3. *Authentication → Configuración → Dominios autorizados* → agregá `TU_USUARIO.github.io`.
4. *Compilación → Firestore Database → Crear base de datos* (modo producción, cualquier región).
5. En Firestore → pestaña *Reglas*: pegá el contenido de `firestore.rules` → Publicar.
6. *Configuración del proyecto* (engranaje) → *Tus apps* → icono `</>` (Web) → registrá la app → copiá el bloque `firebaseConfig`.
7. Pegá esos valores en `firebase-config.js`, subí el cambio al repo y esperá un minuto.

Después, en la app: **Progreso → Iniciar sesión con Google**. Repetí ese paso en cada dispositivo.
Si dos dispositivos cambian cosas al mismo tiempo, gana el último cambio.
