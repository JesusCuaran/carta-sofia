CARTA PARA SOFÍA — CONFIGURACIÓN FIREBASE

IMPORTANTE: el paquete ya tiene la integración de guardado y el panel, pero no puede conectarse hasta que completes los datos de TU proyecto Firebase. No compartas tu contraseña de Google.

A. Crear Firebase
1. Abre https://console.firebase.google.com/ y crea un proyecto.
2. En Project settings (⚙️) > General > Your apps, crea una aplicación Web (</>) y copia la configuración.
3. Pega los valores en firebase-config.js sustituyendo REEMPLAZA...
4. En Build > Firestore Database, crea la base de datos (modo producción).
5. En Build > Authentication > Sign-in method, activa Email/Password.
6. En Authentication > Users, pulsa Add user y crea el correo y contraseña que usarás como administrador.
7. Abre Firestore > Rules, pega el contenido de firestore.rules y reemplaza PON_AQUI_TU_CORREO_ADMIN por el mismo correo administrador. Pulsa Publish.

B. Publicar en GitHub Pages
1. Crea un repositorio en GitHub, por ejemplo carta-sofia.
2. Sube estos cinco archivos a la raíz: index.html, admin.html, firebase-config.js, firestore.rules, README.txt.
   (firestore.rules y README.txt no son necesarios para que la web cargue, pero guárdalos para referencia.)
3. En el repositorio: Settings > Pages > Deploy from a branch > main > /(root) > Save.
4. Espera a que GitHub Pages muestre la URL pública.
5. Carta: abre la URL principal. Panel privado: añade /admin.html al final de la URL.
6. En el panel inicia sesión con el correo y contraseña creados en Firebase Authentication.

C. Probar
1. Abre la carta desde la URL pública y selecciona una respuesta en cada pregunta.
2. Abre /admin.html e inicia sesión. Pulsa Actualizar si no aparece de inmediato.

Privacidad y límites
- Las respuestas incluyen la opción sobre más cartas, la opción de hablar y la fecha/hora. No se recoge nombre ni ubicación.
- Cualquier persona con el enlace puede enviar una respuesta; solo el correo administrador indicado en las reglas puede leerlas.
- No pongas contraseñas en archivos HTML ni compartas la contraseña de administrador.
- Si cambias el correo administrador, actualízalo también en firestore.rules y vuelve a publicar las reglas.
