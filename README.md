# LunaView developer website

Static website for `https://lunaview.net` with English, Portuguese and Spanish public pages.

## Language URLs

- English: `https://lunaview.net/`
- Portuguese: `https://lunaview.net/pt/`
- Spanish: `https://lunaview.net/es/`

Each language includes a home page, support page, privacy policy, terms of service and copyright/content policy.

## Local preview

Run the following from this directory, then open `http://localhost:8080`:

```powershell
python -m http.server 8080
```

The site now uses relative asset paths, so opening `index.html` directly from Explorer also loads its CSS. A local server is still preferred for testing routes and headers.

## Deploy to GitHub Pages

1. Create an empty GitHub repository and push this directory to the `main` branch.
2. In **Settings → Pages → Build and deployment**, choose **GitHub Actions**.
3. The workflow in `.github/workflows/deploy-pages.yml` deploys the site on each push to `main`.
4. Set `lunaview.net` as the custom domain in GitHub Pages and configure the DNS records GitHub Pages requests. Keep the `CNAME` file in the repository.
5. After DNS and HTTPS are active, verify the home page, privacy policy and `https://lunaview.net/app-ads.txt`.

## Required release checks

1. Replace `pub-XXXXXXXXXXXXXXXX` in `app-ads.txt` with the exact AdMob publisher ID from your AdMob account. Google cannot verify an app-ads.txt file without a real publisher ID—never invent one.
2. Audit the final APK/AAB, permissions, SDKs, sign-in, payments, ads and server logs. Update each privacy-policy translation and the Google Play Data safety declaration to match reality.
3. Confirm that all films, posters, trailers, subtitles and trademarks are properly licensed.
4. Complete Google Play’s content rating, target audience, ads declaration, Data safety, app access and privacy-policy forms using the released app’s actual behavior.
5. Have qualified legal counsel review the policies before release, especially if the service is available in multiple jurisdictions, includes subscriptions or accepts user content.
