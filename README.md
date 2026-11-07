# La Morenita: etapa 1

Sitio estático, sin build ni base de datos. Calculador de precios y reserva por WhatsApp.

## Publicar en Vercel

    npx vercel        # vista previa
    npx vercel --prod # producción

Framework Preset: Other. Sin comando de build.

## Planilla de precios

1. Importá `planilla-precios-la-morenita.xlsx` en Google Sheets (Archivo > Importar > Subir).
2. Configurá la planilla en español (Argentina): Archivo > Configuración > Configuración regional.
3. Publicá solo la hoja "Tarifas" como CSV: Archivo > Compartir > Publicar en la web > Tarifas > Valores separados por comas (.csv) > Publicar.
4. Copiá el enlace y pegalo en `index.html`, en `const PLANILLA_CSV='...'`. Volvé a publicar el sitio.
5. Compartí la planilla con el cliente como editor y protegé la columna `codigo` (Datos > Proteger hojas y rangos).

Los cambios tardan unos minutos en verse: Google actualiza el CSV publicado cada pocos minutos.
Si la planilla no responde o un valor no es válido, la página usa los precios guardados en `index.html`.

## Antes de lanzar

- Quitar `noindex` en `index.html` y el bloqueo de `robots.txt`.

## Etapa 2

La versión completa, con reservas online y panel, está guardada aparte (`la-morenita-web.zip`).
