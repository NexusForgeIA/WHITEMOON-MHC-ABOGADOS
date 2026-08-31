# WHITEMOON-MHC-ABOGADOS

Demo web para **MHC Abogados** — despacho de abogados en Cádiz.
Creada por [WhiteMoon Agencia IA](https://whitemoon.es).

- **Demo:** https://nexusforgeia.github.io/WHITEMOON-MHC-ABOGADOS/
- **Web oficial del cliente:** https://mhcabogados.com/

> Esta web es una **demostración**. No es el sitio oficial de MHC Abogados.

## Stack

HTML/CSS/JS puro · GitHub Pages · Supabase (leads + Edge Function de aviso).

## Estructura

```
index.html                              home
aviso-legal/index.html                  aviso legal y privacidad
img/                                    imagenes (WebP + fallback JPG) y logo
og.jpg                                  Open Graph 1200x630
robots.txt · sitemap.xml · llms.txt     SEO / GEO / AEO
supabase/functions/mhc-notify/          Edge Function: aviso por Telegram
```

## Leads

El cliente inserta el lead en `leads_web` (`origen='demo-mhc-abogados'`) con la
publishable key y `fetch keepalive:true`. La Edge Function `mhc-notify` **solo**
notifica por Telegram: no toca la base de datos, asi que la captura no depende
de que responda y no hay filas duplicadas.

## Marca

Blanco + esmeralda. Todo texto en verde usa `#047857` (5.48:1 sobre blanco) o
`#065f46` (7.68:1). `#10b981` y `#34d399` son solo fondos y decoracion: sobre
blanco dan 2.54:1 y 1.92:1 y no cumplen AA.
