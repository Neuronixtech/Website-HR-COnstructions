# HR Constructions — website

Static HTML/CSS/JS website (originally the "Builderz" template from [HTML Codex](https://htmlcodex.com/construction-company-website-template)).

## Structure

| Path | Purpose |
|---|---|---|
| `*.html` | 8 static pages at root (index, about, service, team, portfolio, blog, single, contact) |
| `assets/css/style.css` | All custom styles (2235 lines) |
| `assets/js/main.js` | All custom JS (jQuery, Bootstrap 4 plugins) |
| `assets/vendor/` | Vendored third-party libraries |
| `assets/img/` | Static image assets |

## Preview

No build step required. Open any `.html` file directly in a browser, or serve with any static file server:

```
python3 -m http.server 8000
```

## Libraries (vendored in `assets/vendor/`)

- jQuery, Bootstrap 4 (CDN)
- WOW.js, counterUp, easing, isotope, lightbox, owlcarousel, slick, waypoints

## What's NOT here

- No package.json, no npm/node, no build system
- No CI, no tests, no linter, no formatter

## Deploy on Coolify (Static Site)

1. Connect the repo to Coolify as a **Static Site**
2. Set **Publish Directory** to `.` (or the repo root — all `.html` files are at the root)
3. No Dockerfile needed; Coolify serves the HTML/CSS/JS directly via Nixpacks or its built-in static site proxy
4. Point your domain and Coolify handles SSL/TLS

Edit CSS in `assets/css/style.css`, JS in `assets/js/main.js`, and content in the respective `.html` files.
