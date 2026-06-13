# Hotel Epecuén — Sistema de Restaurante

App web pura (HTML + Firebase) sin servidor, hosteable en GitHub Pages.

## Estructura
```
hotel-epecuen/
  index.html        ← toda la app en un solo archivo
  firestore.rules   ← reglas de seguridad de Firestore
  README.md
```

## Deploy en GitHub Pages

1. Crear repositorio en GitHub (puede ser privado o público)
2. Subir `index.html` al repositorio
3. Ir a Settings → Pages → Source: **Deploy from branch** → branch: `main` → folder: `/ (root)`
4. La URL quedará como: `https://TU-USUARIO.github.io/hotel-epecuen/`

## Configurar Firebase

1. Ir a https://console.firebase.google.com → tu proyecto
2. **Firestore Database** → Reglas → pegar el contenido de `firestore.rules` → Publicar
3. **Authentication** no es necesario (la app usa usuarios guardados en Firestore)

## Primera vez
Al abrir la app por primera vez, se crean automáticamente los usuarios y mesas base.

## Usuarios iniciales
| Usuario | Contraseña | Rol |
|---------|-----------|-----|
| admin   | admin123  | Administrador |
| mozo    | mozo123   | Mozo |
| caja    | caja123   | Caja |
| stock   | stock123  | Stock |
| chef    | chef123   | Chef |
| carhue  | 123       | Recepción Hotel Carhue |

## Colecciones en Firestore
- `usuarios` — usuarios del sistema
- `mesas` — mesas del restaurante
- `comandas` — comandas abiertas
- `comandasDetalle` — items de cada comanda
- `productos` — productos del menú
- `platos` — platos con receta
- `recetas` — ingredientes de cada plato
- `cierres` — cierres de mesa
- `cobros` — cobros realizados por caja
- `historialStock` — movimientos de stock
- `auditoria` — eliminaciones de items
- `vouchers` — vouchers Hotel Carhue
