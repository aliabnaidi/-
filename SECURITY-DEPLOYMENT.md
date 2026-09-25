# SECURITY DEPLOYMENT CHECKLIST

This is a static portfolio, so its attack surface is already relatively small.
No website can be guaranteed to be impossible to hack.

Before publishing:
1. Publish it over HTTPS only.
2. Keep the included `_headers` file on hosts that support it (Netlify/Cloudflare Pages style).
3. Keep `.htaccess` on Apache hosting.
4. Do not add API keys, passwords, database credentials, private tokens, or server configuration files to the public folder.
5. If you later add a backend/contact form, validate and sanitize all server-side input and add rate limiting/CSRF protection.
6. Keep dependencies and third-party scripts to a minimum.
7. The site uses a Content Security Policy and several security headers; test the deployed site after publishing.
8. If using GitHub Pages, `_headers` and `.htaccess` are not applied by GitHub Pages, but the browser-side CSP in `index.html` still applies. Configure equivalent headers through your hosting/CDN if available.
