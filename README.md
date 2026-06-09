# SLOB Manager — IMPROM SA

Web app para gestionar el inventario SLOB (Slow-Moving & Obsolete).

## Fuente de datos

- **Sheet ID:** `1mPK2pIRGZNFP5NSuQHreG6Mhn208uy7zaIsCMqhF-Ng`
- **Hoja:** Gestión SLOB (GID `1111014850`)

Para que el fetch automático funcione, el dueño del sheet debe publicarlo:
> Google Sheets → Archivo → Compartir → **Publicar en la web** → Hoja "Gestión SLOB" → CSV → Publicar

Esto NO cambia los permisos de edición; solo habilita la lectura pública del CSV.

## Estructura esperada del CSV

| Fila | Contenido |
|------|-----------|
| 1 | Título con `Actualizado: DD/MM/YYYY HH:mm` |
| 2 | Headers de resumen (SLOBs, Valorizado, % Catálogo) |
| 3 | Valores de resumen (521, USD 1.409.169, 61.0%) |
| 4 | Vacía |
| 5 | Headers: `#, Código, Nombre, Familia, Marca, Origen, ABC, Stock actual, Costo USD, Valorizado USD, Prom. mes, Cobert (m), Tendencia, Responsable, Revisión, Notas` |
| 6+ | Datos |

## Publicar en GitHub Pages

```bash
git init
git add index.html README.md
git commit -m "SLOB Manager"
git remote add origin https://github.com/IMPROM/slob-manager.git
git push -u origin main
```
Luego: Settings → Pages → Branch: main / root → Save.

## Sin internet / sheet privado

Usar botón **CSV** en la app:
1. Google Sheets → Archivo → Descargar → CSV
2. Abrir con Bloc de Notas → Ctrl+A → Ctrl+C
3. Pegar en el modal de la app → Cargar
