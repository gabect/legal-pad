# Legal Pad Cloud

Bloc de notas amarillo alojado en GitHub Pages, con Google Authentication y Firestore.

## Antes de usar

1. En Firebase Console > Authentication > Sign-in method, activa Google.
2. En Authentication > Settings > Authorized domains, agrega `gabect.github.io`.
3. En Firestore Database, crea una base de datos en Production mode.
4. En Firestore Database > Rules, pega el contenido íntegro de `firestore.rules` y pulsa Publish. Las reglas del repositorio **no se aplican automáticamente**.
5. En GitHub > repositorio legal-pad > Settings > Pages > Build and deployment, elige Deploy from a branch, `main`, carpeta `/(root)`, y Save.
6. Abre https://gabect.github.io/legal-pad/ e inicia sesión; verifica crear, editar, recargar y abrir desde un segundo dispositivo.

**Privacidad:** el código de la web es público, pero las notas se almacenan en Firestore y sus reglas deben restringirlas al propietario. No guardar contraseñas ni datos muy sensibles: no hay cifrado de extremo a extremo.

**Límites:** Sincronización requiere conexión; Spark tiene cuotas; la edición simultánea del mismo documento puede sobrescribir cambios (último guardado gana). Verifica las reglas y el inicio de sesión antes de almacenar notas personales.
