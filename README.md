# Bir Acro Team

A responsive React website for Bir Acro Team in Bir Billing. A charcoal, cream and lime visual system frames real flying footage, an interactive canvas maneuver explorer, film dialogs, a dedicated Shorts section, two member profiles and Instagram enquiry links.

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
- Shorts layout and native players: `src/shorts.css`
- Main page and social links: `src/main.jsx`
- Responsive styling and animation: `src/style.css`; full-frame video layout: `src/video-layout.css`
- Locally saved images and optimized video: `public/media/`
- Research and media credits: `SOURCES.md`

The compact hero headline overlays edge-to-edge background footage on desktop and phones. The background fills the hero without a separate video box; the full original framing remains available in the film player. Landscape and portrait film cards preserve their original frame proportions. The hero contains a 27.7-second uncropped 1080p montage from the YouTube film supplied by the user. It includes the aerial shot at 00:41–00:45, infinity tumbling at 00:51–01:10, and the landing at 00:20–00:24.7. It starts muted, has pause and sound controls, and uses a local poster fallback. Motion is paused initially when the visitor requests reduced motion. The full original film opens in a YouTube player; the Instagram reel opens in its original platform embed. Both have direct source links when the platform restricts embedded playback. Two additional Shorts from the Bir Acro Team YouTube channel play locally in native portrait video players with pause, sound, scrubbing and fullscreen controls. The selected 26-second clip is featured first. The background video pauses while a film dialog is open and resumes according to the visitor’s existing pause setting when it closes.

SAT, helicopter and infinity tumbling animations are artistic illustrations. They are not physical simulations or flying instructions. The controls support pause, half speed and keyboard selection. Film dialogs support Escape and restore keyboard focus. The page includes a mobile navigation menu, expandable FAQs, and an enquiry message copier.

Member cards feature Sonu Rajput (`@airbornesoul`) and Gourav (`@fly__with__me____`). Both publicly identify as founders of Bir Acro Team and paragliding instructors; Sonu identifies as an acro pilot and Gourav as a freestyle pilot. Additional members, achievements, prices and flight availability should be confirmed with the team before adding them.

## Validation

Production build passed. Chrome checks passed at viewport widths 320, 390, 768 and 1440 pixels with no horizontal overflow or JavaScript runtime errors. Verified local video loading and playback, pause and mute, maneuver keyboard navigation, film dialog open/close, FAQ expansion, enquiry selection and clipboard, mobile menu, and image loading.

## Hosting

The site uses GitHub Pages at [bir-acro-team.github.io](https://bir-acro-team.github.io/).

The workflow in `.github/workflows/pages.yml` installs locked dependencies, builds the site, and deploys the `dist/` artifact whenever `main` changes. It can also be run manually from the repository’s Actions tab. GitHub Pages is configured to use GitHub Actions as its publishing source.

The repository name matches the organization’s Pages domain, so root-relative image, video, and asset paths work without a project subdirectory. Original media credits are maintained in `SOURCES.md` and on the website.
