# Hogue Applications LLC website

A lightweight static company website for https://hogueapplications.com. Built with plain HTML and a shared CSS file. No JavaScript, packages, build step, external fonts, or third-party images are required.

## Site structure

- `index.html` — company homepage and Our Apps feature.
- `injury-report.html` — Injury Report features and App Store link.
- `support.html` — app information and guidance for describing issues.
- `privacy.html` — existing Injury Report privacy policy, reproduced with its September 6, 2026 revision date and a source link.
- `contact.html` — clickable company email and support link.
- `404.html` — GitHub Pages not-found page.
- `assets/css/styles.css` — shared layout, typography, light/dark colors, and responsive styles.
- `CNAME` — intended custom domain: `hogueapplications.com`.
- `.nojekyll` — lets GitHub Pages serve the files directly without Jekyll processing.

## Preview locally

For a quick preview, open `index.html` in a browser. Internal links work directly from the filesystem.

For an HTTP preview, if Python 3 is installed, open a terminal in this repository and run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then visit http://localhost:8000. Press Control+C in the terminal to stop the server. No dependencies need to be installed.

Check a narrow phone width, tablet width, and desktop width. The website follows the device/browser light or dark appearance setting. Try Tab navigation to check the skip link, navigation, and buttons.

## Editing content

Edit the relevant HTML file in a text editor. Every page is standalone; when changing shared header or footer content, apply the same change to all six HTML files. Keep one main heading (`h1`) on each page and descriptive link text.

Edit the color variables at the start of `assets/css/styles.css` for the light theme and in the `prefers-color-scheme: dark` block for the dark theme. The mobile layout is in the `max-width: 760px` block. All ordinary internal links and stylesheet references are relative, so the main pages support a GitHub Pages project path as well as the custom domain.

The 404 page is a special case: GitHub Pages can display it at any nested missing URL. Its `base` element points to the intended custom domain so navigation and CSS resolve correctly there. Before using the site on a GitHub project URL without the custom domain, change that base URL and its home button to the actual Pages base URL (including the repository path and trailing slash). A local Python server does not automatically serve `404.html` for missing routes; visit it directly to inspect its content. Its stylesheet and links use the configured domain unless you temporarily change the base URL for local preview.

## Contact and privacy content

The public contact address is `injuryreportapp@gmail.com`. Clickable email links appear on the Contact, Support, and Privacy pages. Keep these three pages consistent when changing the contact address.

The Privacy page reproduces the existing [Injury Report privacy policy](https://docs.google.com/document/d/1-kZEhdO_pMPNYuFLu7gHyzxwWSYGh38ztTcIzUn0pC8/edit?usp=drivesdk), last updated September 6, 2026. Its wording, including the existing App Store support-contact paragraph, is preserved. A source link and clickable email appear separately below the policy. No replacement legal language was drafted. Future policy edits should be supplied or approved by the owner.

There are no remaining user-facing content placeholders. Review the company/app copy and migrated policy before publishing. No logo or image assets are required. The current identity is text only; the decorative app panel is typography and CSS, not an app screenshot.

## GitHub Pages and custom domain

The repository is prepared for static hosting from its root. `CNAME` contains only `hogueapplications.com`. No deployment workflow is necessary for branch-based GitHub Pages hosting.

Publishing is a separate, explicitly authorized step: configure GitHub Pages to serve the intended branch’s root, configure the custom domain, and arrange DNS separately in Cloudflare. No DNS values are prescribed here. Once domain setup is complete, verify HTTPS and every page, including a nested nonexistent URL to test the 404 page.

No deployment, push, DNS changes, or remote repository settings were performed as part of creating these files. This site makes no guarantee about Apple Developer Program verification; review the public information before submitting it as the organization website.
