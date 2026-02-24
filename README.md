# Kungarum.se — LM Schön

Webbplats för författaren LM Schön (Linda Schön).

## Innehåll

- **Böcker:** Jasmin och Eddie-serien (9–12 år), Lena Fredén-serien (vuxendeckare)
- **Om författaren:** Bakgrund, biografi, mission
- **Föreläsningar:** Skolbesök och föreläsningar för alla åldrar
- **Kontakt:** Formulär via Formspree

## Teknik

Statisk webbplats (HTML/CSS/JS), hostad på Azure Static Web Apps.

## Setup

### Formspree

1. Skapa konto på [formspree.io](https://formspree.io)
2. Skapa nytt formulär och kopiera form-ID
3. Ersätt `YOUR_FORM_ID` i `index.html` med ditt ID

### Azure Static Web Apps

1. Skapa en Static Web App i Azure Portal
2. Koppla till detta GitHub-repo
3. Lägg till `AZURE_STATIC_WEB_APPS_API_TOKEN` som repository secret
4. Push till `main` triggar auto-deploy

### DNS (webb.se)

1. Logga in på webb.se
2. Lägg till CNAME-post: `www` → `<din-azure-app>.azurestaticapps.net`
3. Lägg till CNAME/TXT för apex-domänen enligt Azure-instruktioner
4. Konfigurera custom domain i Azure Portal
