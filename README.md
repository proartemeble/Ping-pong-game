# SpotiArt Studio — Landing Page

Statyczny, jednostronicowy (one-page) landing page dla **SpotiArt Studio** (https://spotiart.pl/) —
prywatnego, przeglądarkowego centrum muzycznego. Strona jest dopracowana pod kątem **SEO**
oraz **GEO** (optymalizacja pod wyszukujące roboty i modele AI).

## Zawartość

| Plik | Opis |
|------|------|
| `index.html` | Cała strona (semantyczny HTML5, wbudowany CSS i minimalny JS — zero zależności zewnętrznych). |
| `favicon.svg` | Ikona marki (wektorowa). |
| `robots.txt` | Reguły dla robotów, w tym jawne zezwolenia dla crawlerów AI (GPTBot, ClaudeBot, PerplexityBot, Google-Extended…). |
| `sitemap.xml` | Mapa strony. |
| `llms.txt` | Zwięzły opis dla modeli AI (standard llms.txt) — GEO. |
| `site.webmanifest` | Manifest PWA. |
| `assets/og-image.png` | Obraz Open Graph / Twitter (1200×630). |
| `assets/icon-*.png` | Ikony aplikacji (180/192/512). |

## Optymalizacja SEO / GEO

- Semantyczny HTML5, atrybut `lang="pl"`, hierarchia nagłówków, `alt`/ARIA, skip-link.
- Kompletne meta: `title`, `description`, `keywords`, `robots`, **canonical**.
- **Open Graph** i **Twitter Cards** z obrazem 1200×630.
- **Dane strukturalne JSON-LD**: `Organization`, `WebSite`, `SoftwareApplication`, `FAQPage`.
- Sekcja **FAQ** z pytaniami i odpowiedziami (sprzyja fragmentom rozszerzonym i odpowiedziom AI).
- `robots.txt` + `sitemap.xml` + **`llms.txt`** dla wyszukiwarek i modeli generatywnych.
- Wydajność: brak zewnętrznych zasobów, wbudowany CSS/JS, `prefers-reduced-motion`.
- Responsywność (desktop / tablet / mobile) i motyw dopasowany do marki (dark + neon green).

## Uruchomienie

Strona jest w pełni statyczna — wystarczy dowolny serwer plików lub otwarcie `index.html`:

```bash
python3 -m http.server 8080
# następnie: http://localhost:8080
```

## Wdrożenie

Wgraj zawartość katalogu na dowolny hosting statyczny (np. Netlify, Vercel, GitHub Pages,
Cloudflare Pages) lub serwer WWW obsługujący domenę `spotiart.pl`. Przed publikacją produkcyjną
upewnij się, że adresy w `canonical`, `sitemap.xml`, Open Graph i JSON-LD wskazują docelową domenę.
