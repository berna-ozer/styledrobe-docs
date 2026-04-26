# Styledrobe — Public Docs

Bu repo Styledrobe iOS uygulamasının yasal sayfalarını yayınlar (Privacy Policy + Terms of Service). Apple App Store Review için zorunlu.

App'in kaynak kodu private bir repo'da; bu repo sadece public-facing dökümanlar içindir.

## URLs

- Landing: https://berna-ozer.github.io/styledrobe-docs/
- Privacy: https://berna-ozer.github.io/styledrobe-docs/privacy/
- Terms:   https://berna-ozer.github.io/styledrobe-docs/terms/

## GitHub Pages aktive etme

1. https://github.com/berna-ozer/styledrobe-docs/settings/pages
2. Source: **Deploy from a branch**
3. Branch: `main` / Folder: `/ (root)` → Save
4. 1-2 dk sonra yukarıdaki URL'ler açılır.

## Custom domain (opsiyonel)

Domain alındıktan sonra (örn. `styledrobe.app`):

1. DNS A records:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
2. CNAME `www` → `berna-ozer.github.io`
3. `CNAME` dosyası ekle (içeriği: `styledrobe.app`)
4. Pages settings → Custom domain → Save → Enforce HTTPS
