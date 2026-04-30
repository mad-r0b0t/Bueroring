# 🏢 BÜRORING eG – Moderne B2B Landingpage

Eine hochkonvertierende, moderne Single-Page-Website für die **BÜRORING eG** und die **büroforum AG**. Das Design orientiert sich an modernen SaaS-Standards (ähnlich Notion, Linear oder Stripe) und zeichnet sich durch klare Typografie, strategischen Weißraum und subtile Animationen aus.

## ✨ Features

- **All-in-One File**: Die gesamte Landingpage besteht aus einer einzigen Datei (`index.html`) – HTML, CSS und JavaScript sind inline integriert.
- **Modernes B2B-Design**: Professionelle Farbpalette, klare visuelle Hierarchie und Einsatz von Google Fonts (Outfit).
- **Zero Dependencies**: Kein jQuery, kein Bootstrap, kein Tailwind. 100% Vanilla JS und natives CSS.
- **Performance-Optimiert**: Verzicht auf externe Icon-Bibliotheken (alle Icons sind Inline-SVGs). Einziger externer Request ist Google Fonts via CDN.
- **Scroll-Animationen**: Flüssige Fade-In-Effekte beim Scrollen mithilfe der nativen `IntersectionObserver` API.
- **Interaktive Counter**: Animierte Zahlen-Statistiken, die starten, sobald sie in den Viewport scrollen.
- **Mobile-First & Responsive**: Perfekte Darstellung auf allen Endgeräten dank CSS Grid, Flexbox und optimierten Breakpoints.
- **Datenschutz (GDPR/DSGVO)**: Kein externes Tracking, keine Cookies, keine Third-Party-Skripte (außer Fonts).

## 🛠️ Technologien

- **HTML5**: Semantischer Aufbau (`<header>`, `<main>`, `<section>`, `<footer>`).
- **CSS3**: CSS Custom Properties (Variables), CSS Grid, Flexbox, moderne Hover-States und Backdrop-Filter.
- **JavaScript (ES6)**: Vanilla JS für Mobile-Menü, Sticky Navigation, Smooth Scrolling, Intersection Observers und Formular-Feedback.

## 🎨 Design-Spezifikationen

### Typografie
- **Font-Family**: `Outfit` (sans-serif)
- Gewichte: 300 (Light), 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold), 800 (ExtraBold)

### Farbpalette
- 🔵 **Primary (`#1A3A5C`)**: Dunkelblau für Vertrauen und B2B-Fokus.
- 🟠 **Accent (`#E8A020`)**: Warmes Orange/Gold für Call-to-Actions und visuelle Highlights.
- ⚪ **Background (`#F8F9FC`)**: Ein kühles Fast-Weiß für besseren Kontrast zu den weißen Cards.
- ⚫ **Text (`#1C1C2E`)**: Sehr dunkles Blau/Grau für optimale Lesbarkeit.

## 🚀 Installation & Nutzung

Da es sich um eine reine statische HTML-Datei handelt, ist kein Build-Prozess oder lokaler Server zwingend erforderlich.

1. Lade die Datei `index.html` herunter.
2. Öffne die Datei per Doppelklick in einem beliebigen modernen Webbrowser (Chrome, Firefox, Safari, Edge).
3. **Für Entwickler**: Um das Verhalten realistischer zu testen (z.B. für mobile Tests im selben Netzwerk), empfiehlt sich die Nutzung einer Extension wie "Live Server" in VS Code.

## 📝 Anpassungen vornehmen

### Links zu externen Systemen
Die Links zum Extranet und zum Shop sind bereits vorbereitet. Suche im Code nach folgenden Stellen, um sie ggf. anzupassen:
- `https://extranet.bueroring.de` (Händler-Login)
- `https://brshop.bueroring.de/frontpage` (brShop24)

### Kontaktformular
Das Kontaktformular hat aktuell einen reinen Frontend-Dummy-Handler (JavaScript Event-Listener auf `id="contactForm"`), der visuelles Feedback gibt. 
Um echte E-Mails zu versenden, musst du das `action`-Attribut im `<form>`-Tag auf deinen Backend-Endpunkt anpassen (z.B. PHP-Skript, Formspree oder Netlify Forms) und den `e.preventDefault()` im `<script>`-Bereich entfernen oder für einen Fetch/XHR-Request umbauen.

### Bilder & Grafiken
Alle Grafiken (inklusive der Hero-Grafik und der Standort-Karte) wurden als skalierbare, abstrakte **Inline-SVGs** direkt im Code generiert, um die Ladezeit zu minimieren. Wenn echte Fotos verwendet werden sollen, können die entsprechenden `<svg>`-Tags einfach durch `<img src="...">` ersetzt werden.

## ♿ Barrierefreiheit (a11y)
Das Projekt nutzt semantisches HTML, klare Kontraste nach WCAG AA-Richtlinien und `aria-labels` für interaktive Elemente ohne Text (z.B. das Mobile-Hamburger-Menü und Social-Media-Icons), um die Bedienbarkeit für alle Nutzer zu gewährleisten.
