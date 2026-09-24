# EchoPhish — GoDaddy cPanel Upload Guide
==========================================

## Files in this package:
- index.html        → Main website (homepage)
- 404.html          → Custom 404 error page
- coming-soon.html  → Coming soon / launch countdown page
- .htaccess         → Apache config (HTTPS, routing, security, caching)
- robots.txt        → Search engine crawler rules
- sitemap.xml       → SEO sitemap (update domain if needed)
- README.txt        → This file

==========================================
## HOW TO UPLOAD TO GODADDY CPANEL
==========================================

### METHOD 1 — File Manager (Easiest)
1. Log in to GoDaddy → My Products → Web Hosting → Manage
2. Click "cPanel Admin"
3. In cPanel, open "File Manager"
4. Navigate to the "public_html" folder
5. Click "Upload" and upload ALL files from this folder
   ⚠️  Make sure .htaccess is included (enable "Show Hidden Files")
6. Done! Visit your domain to confirm it's live.

### METHOD 2 — FTP (FileZilla)
1. In cPanel → FTP Accounts, note your FTP credentials
2. Open FileZilla → File → Site Manager → New Site
   - Host: your domain or server IP
   - Protocol: FTP or SFTP
   - User/Pass: your cPanel credentials
3. Connect and drag all files into the "public_html" folder

==========================================
## USING THE COMING SOON PAGE
==========================================

To make the coming-soon page your homepage temporarily:
  - Rename index.html → main.html
  - Rename coming-soon.html → index.html

To set a launch date, open coming-soon.html and edit line:
  const launchDate = new Date(2026, 5, 1, 0, 0, 0);
  Format: (YEAR, MONTH-1, DAY, HOUR, MIN, SEC)
  Example: June 1 2026 = (2026, 5, 1, 0, 0, 0)

==========================================
## IMPORTANT NOTES
==========================================

✅  Upload to "public_html" — NOT a subfolder
✅  Replace "echophish.com" in sitemap.xml with your actual domain
✅  Enable SSL first (cPanel → Security → Let's Encrypt SSL)
✅  .htaccess forces HTTPS — SSL must be active before uploading

==========================================
