# Jordi Cervero — industrial consulting site

Static HTML/CSS/JS site for GitHub → Netlify. The contact form uses Netlify Forms. No Node dependencies, server function or external form service are needed.

## Files

- `index.html`: home, services, method, experience, SME support, credentials and contact form
- `operations.html`, `project-site-management.html`, `process-safety.html`, `occupational-safety.html`, `digital-transformation.html`: service pages
- `privacy.html`: contact privacy notice; review before launch
- `thanks.html`: confirmation after a successful submission
- `assets/css/theme.css`, `assets/js/main.js`: styling and basic site interaction

## Publish and activate notifications

1. Connect this GitHub repository to Netlify; use the repository root as the publish directory and leave the build command empty. Enable form detection in the site's Forms settings if needed.
2. Deploy. Netlify detects the static `<form name="contacto" data-netlify="true">` during deployment.
3. In the Netlify site dashboard, go to **Forms → Submission notifications → Add notification → Email notification** and enter the Gmail address that should receive new enquiries.
4. Review `privacy.html`, then send a real test enquiry on the deployed site. Confirm that it appears under Forms, that the notification reaches Gmail and that `thanks.html` appears after submission.

The honeypot field reduces automated spam. The form works without JavaScript. Do not open `index.html` directly as a local file to test delivery; Netlify must first deploy and detect it.
