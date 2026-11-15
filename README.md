# FleetSafe Landing Page

Static landing page for **FleetSafe**, the preventive safety control platform for freight fleets built by **BitMeisters**.

Course: 1ASI0729 Desarrollo de Aplicaciones Open Source · Universidad Peruana de Ciencias Aplicadas.

## Stack

- HTML5, CSS3 and vanilla JavaScript. No build step and no frameworks.
- Design tokens implemented as CSS custom properties.
- Internationalization for `en-US` and `es-419`, with English as the default language. The chosen language is kept in the browser.
- Accessibility following WAI-ARIA: skip link, labelled controls, a live region that announces language changes, visible keyboard focus and reduced motion.
- Videos embedded from YouTube through `youtube-nocookie.com`.

## Structure

```
index.html          home page
terms.html          terms of use, linked from the footer
privacy.html        privacy policy, linked from the footer
assets/
  css/
    styles.css      design tokens, layout, components and sections of the home page
    legal.css       terms of use and privacy policy pages
  i18n/
    en-US.js        English dictionary
    es-419.js       Spanish dictionary
  js/
    main.js         language, navigation, sample inspection, videos and links to the platform
    legal.js        language of the terms of use and privacy policy pages
  images/
    favicon.svg     site icon
    photos/         photos of the home page
    team/           team photos
```

## Sections of the home page

Hero, the problem, the platform (with the About the Product video), how it works, roles, subscription plans, the team (with the About the Team video), frequently asked questions and the final call to action.

## Running locally

There is nothing to build. Open `index.html`, or serve the folder with any static server, such as the Live Server extension of Visual Studio Code or `python -m http.server`. The YouTube videos may not play when the file is opened directly, so use a server to see them.

## Configuration

The constants at the top of `assets/js/main.js` set the links of the page:

| Constant | Purpose |
|---|---|
| `PLATFORM_URL` | URL of the web application. Every button of the page opens its sign-in screen, `iam/sign-in` |
| `PRODUCT_VIDEO` | unlisted YouTube link of the About the Product video |
| `TEAM_VIDEO` | unlisted YouTube link of the About the Team video |

While a video link is empty, its section shows a placeholder. Each video needs embedding to be allowed in YouTube Studio.

## Translations

Every visible text carries a `data-i18n` key. To add or change a text, set the same key in `assets/i18n/en-US.js` and `assets/i18n/es-419.js`.

## Deployment

Published on GitHub Pages at https://1asi0729-2620-16692-bitmeisters.github.io/fleet-safe-website.

The calls to action send the visitor to the sign-in screen of the web application deployed at https://1asi0729-2620-16692-bitmeisters.github.io/fleet-safe-web-application/iam/sign-in.

## Related repositories

- `fleet-safe-web-application`: Angular web application of FleetSafe.
- `fleet-safe-web-services`: RESTful API of FleetSafe built with Spring Boot.

## Conventions

- **GitFlow**: `main` holds released versions, `develop` integrates work, and every feature lives in its own `feature/<kebab-case-name>` branch.
- **Conventional Commits** for every commit message.
- **Semantic Versioning** for every release.

## Team

BitMeisters — Universidad Peruana de Ciencias Aplicadas.