# Costos Sanguchería Anónima

App estática (sin build). Archivos:
- index.html: la app
- firebase-config.js: la config de Firebase (completar)
- datos-iniciales.json: insumos y sanguches precargados. Se usan solo la primera vez que la base está vacía.

## 1. Firebase (para que celu y compu vean lo mismo)
1. Podés usar el mismo proyecto de Firebase de la app de pedidos. En Configuración del proyecto > Tus apps > Web, copiá el objeto firebaseConfig y pegalo en firebase-config.js.
2. Los datos quedan en la colección `costeo`, documento `estado`.
3. En las reglas de Firestore agregá:
   match /costeo/{doc} { allow read, write: if true; }
   Ojo: así cualquiera que tenga el link puede ver y editar. Más adelante se le puede agregar login.

Sin config, la app funciona igual pero guarda solo en el navegador donde la abrís.

## 2. Vercel
Opción A (CLI, desde esta carpeta): npx vercel --prod
Opción B: subí la carpeta a un repo de GitHub, entrá a vercel.com > Add New > Project > importá el repo. Framework: Other. Sin build command.

## 3. En el celu
Abrí el link y usá "Agregar a pantalla de inicio" para tenerla como app.
