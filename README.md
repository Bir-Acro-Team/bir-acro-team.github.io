# Bir Acro Team

A responsive React website for Bir Acro Team in Bir Billing. A charcoal, cream and lime visual system frames real flying footage, an interactive canvas maneuver explorer, film dialogs, a dedicated Shorts section, three pilot profiles and Instagram enquiry links.

## Run locally

```sh
git clone https://github.com/Bir-Acro-Team/bir-acro-team.github.io.git
cd bir-acro-team.github.io
npm install
npm run dev
```

For a production build, run `npm run build`. Serve `dist/` with any static host. `npm run preview` previews that build locally. The site has no backend, environment variables or paid dependencies. The enquiry buttons open Instagram directly; no enquiries are collected or stored on the site.

## Content

- Logo: `public/media/team-logo.webp`, sourced from the Facebook page supplied by the user
- Wider team layout and feature player: `src/team.css`
- Shorts layout and native players: `src/shorts.css`
- Main page and social links: `src/main.jsx`
- Responsive styling and animation: `src/style.css`; full-frame video layout: `src/video-layout.css`
- Locally saved images and optimized video: `public/media/`
- Research and media credits: `SOURCES.md`

The page centres the wider Bir Billing flying community. The hero reads “ACRO IS NOT A CRIME”. An origin-story section adapts the user’s Hindi/Hinglish account of plastic gliders, the 2015 acro display, joining AntiGravity after Class 12, the secret 5 a.m. training routine, and the first-flight video shown to family. It does not assign the recollection to an individual. Abhishek (Abu), Gaurav (Mithu) and Sonu have individual profiles and photographs, with additional voices from Rakesh, Krishna and Akshu Thakur. The lead feature is **Acro Is Not a Crime — It’s a Calling**, the 84-second film supplied by the user. Its complete original 1276×720 video is hosted locally at `public/media/acro-calling.mp4`, remuxed with fast-start metadata and no video re-encoding. The player has native pause, sound, scrubbing and fullscreen controls, and credits Fullsend Himalayas, director/editor @acha_sa_naam and DOP @abhixdoon. Sonu’s earlier YouTube film remains as a supporting story.

The 33.2-second hero montage opens with the requested ground-gliding/landing shot (the original YouTube film at 00:20–00:24.7). It then uses the new team feature at 00:15–00:20.5, 00:48–00:54.5 and 01:00–01:06.5, followed by the original film at 00:41–00:45 and 00:51–00:57. The montage is normalized to 1920×1080 at 30 fps; the team film’s native resolution is 1276×720. Compact text overlays the edge-to-edge footage, which starts muted and offers pause and sound controls. Reduced-motion visitors initially see a still poster.

Landscape and portrait film cards preserve their proportions. Two Bir Acro Team Shorts play locally, and the earlier Instagram reel is embedded from its source. The background pauses whenever a film dialog opens and resumes according to the visitor’s existing pause setting when it closes. Dialogs close with Escape and restore keyboard focus.

SAT, helicopter and infinity tumbling animations are artistic illustrations. They are not physical simulations or flying instructions. The controls support pause, half speed and keyboard selection. Film dialogs support Escape and restore keyboard focus. The page includes a mobile navigation menu, expandable FAQs, and an enquiry message copier.

Member cards feature Abhishek (`@acroliglide_`), Gaurav (`@fly__with__me____`) and Sonu Rajput (`@airbornesoul`). Abhishek’s Instagram identifies him as an acro pilot, instructor and member of both teams. The new feature labels Abhishek as Abu and Gaurav as Mithu. The display spelling Gaurav follows the film and the user’s supplied caption; his Instagram currently spells the name Gourav. Sonu’s profile remains alongside the other pilots. No new membership or founder status is inferred for the three local pilots interviewed in the film.

## Validation

Production build passed. Chrome checks passed at viewport widths 320, 390, 768 and 1440 pixels with no horizontal overflow or JavaScript runtime errors. Verified local video loading and playback, pause and mute, maneuver keyboard navigation, film dialog open/close, FAQ expansion, enquiry selection and clipboard, mobile menu, and image loading.

## Hosting

The site uses GitHub Pages at [bir-acro-team.github.io](https://bir-acro-team.github.io/).

The workflow in `.github/workflows/pages.yml` installs locked dependencies, builds the site, and deploys the `dist/` artifact whenever `main` changes. It can also be run manually from the repository’s Actions tab. GitHub Pages is configured to use GitHub Actions as its publishing source.

The repository name matches the organization’s Pages domain, so root-relative image, video, and asset paths work without a project subdirectory. Original media credits are maintained in `SOURCES.md` and on the website.
