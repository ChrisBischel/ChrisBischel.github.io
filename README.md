# Personal Stream Deck Assistant — GitHub Pages site

Prepared for a personal Google OAuth application used with Danex360's Google Assistant plugin for Elgato Stream Deck.

## Upload (GitHub web interface; no coding required)
1. Open https://github.com/new and create a **Public** repository named EXACTLY `<your-GitHub-username>.github.io` (use your actual GitHub username). Do not choose a README or other starter files.
2. On the new repository's Code tab, choose **Add file → Upload files** (or the upload link), and upload `index.html`, `privacy.html`, `terms.html`, `style.css`, and `.nojekyll` from this package. Commit to `main`.
3. Open **Settings → Pages → Build and deployment**. Choose **Deploy from a branch**, then `main` and `/(root)`; Save.
4. Your URLs, once live, should be:
   - Home: `https://<your-GitHub-username>.github.io/`
   - Privacy: `https://<your-GitHub-username>.github.io/privacy.html`
   - Terms: `https://<your-GitHub-username>.github.io/terms.html`
5. Visit all three pages while signed out or using a private window, checking content and links.
6. In Google Cloud → Google Auth Platform → Branding, insert the 3 URLs into the respective App domain fields. If prompted for an Authorized Domain, try `<your-GitHub-username>.github.io` and check Google Cloud's exact requirement.
7. Verify site ownership in Google Search Console (https://search.google.com/search-console) using URL-prefix property `https://<your-GitHub-username>.github.io/`, usually by uploading Google's exact HTML verification file to the repository root (then verify the file publicly loads). Google's OAuth domain ownership verification may have additional requirements.
8. Try to publish under Google Cloud → Google Auth Platform → Audience. After publishing, remove and re-add the plugin's Google account authorization for a fresh refresh token.

## Important limitations
- This GitHub Pages URL is on a shared hosting platform. Google explicitly requires a verified domain you control and may reject `github.io` during OAuth brand verification despite Search Console verification. A custom domain may ultimately be necessary. This package does NOT guarantee Google approval.
- This site is informational; it does not authenticate, execute Google Assistant commands, or store tokens.
- Review the drafted statements and compare with the plugin developer's current privacy notice before using the site publicly; the scope declarations and token handling are based on the developer's published privacy policy as of Nov 2026.
- Do not put OAuth client secrets, refresh tokens, or Google credentials in any GitHub repository, especially a public one.

References:
- Developer privacy: https://danex360.com/proyectos/streamdeck-assistant/privacidad
- Google brand verification: https://developers.google.com/identity/protocols/oauth2/production-readiness/brand-verification
- GitHub Pages branch publishing: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
