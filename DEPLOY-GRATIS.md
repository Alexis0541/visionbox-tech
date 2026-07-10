# Publicar gratis: GitHub Pages + DigitalPlat + Cloudflare

## 1. GitHub Pages

1. Crea un repositorio publico en GitHub, por ejemplo `streamcolombia`.
2. Sube estos archivos a la raiz del repositorio:
   - `index.html`
   - `.nojekyll`
3. En GitHub entra a `Settings > Pages`.
4. En `Build and deployment`, usa:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Guarda. El sitio queda en:
   `https://TU_USUARIO.github.io/streamcolombia/`

## 2. Dominio gratis en DigitalPlat

1. Entra a `https://dash.domain.digitalplat.org/`.
2. Solicita un nombre disponible, por ejemplo:
   `streamcolombia.dpdns.org`
3. Elige Cloudflare como proveedor DNS si te lo permite el panel.

## 3. Cloudflare DNS hacia GitHub Pages

Para un subdominio como `streamcolombia.dpdns.org`, crea:

```text
Tipo: CNAME
Nombre: streamcolombia
Destino: TU_USUARIO.github.io
Proxy: DNS only al inicio
```

Luego en GitHub, en `Settings > Pages > Custom domain`, escribe:

```text
streamcolombia.dpdns.org
```

Cuando GitHub valide el dominio, activa `Enforce HTTPS`.

