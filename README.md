# InventarioDon

Copia independiente del sistema de inventario y ventas, preparada para usar una base Firebase distinta.

## Importante

- No trae la configuracion Firebase original.
- Crea `public/firebase-config.js` a partir de `public/firebase-config.example.js`.
- `public/firebase-config.js` esta en `.gitignore` para no subir credenciales/configuracion al repo.
- Esta version permite vender aunque el stock llegue a 0; el stock puede quedar negativo.

## Configuracion Firebase

1. Copia el archivo de ejemplo:

```bash
copy public\firebase-config.example.js public\firebase-config.js
```

2. Cambia los valores por los de tu nuevo proyecto Firebase.
3. Agrega los correos autorizados en `authorizedEmails`.

Si `authorizedEmails` queda vacio, cualquier cuenta Google aceptada por Firebase Auth podra entrar.

## Ejecutar local

```bash
npm install
npm start
```

Abre `http://localhost:3000`.

## Hosting recomendado

Para esta copia conviene Firebase Hosting porque la app ya usa Firebase y no necesita servidor propio para funcionar. Railway solo seria necesario si despues se agrega un backend privado o integraciones de servidor.
