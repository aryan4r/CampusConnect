# CampusConnect — LPU Event Portal

A static campus event discovery and registration portal for Lovely Professional University (LPU), Phagwara, Punjab. Students can browse upcoming events, filter them by category, and open a registration form, all without any JavaScript.

## Features

- **Home page** with a hero section, campus highlights, a featured event spotlight (Innovate 2026), a preview of upcoming events, and a "How it works" section.
- **Events page** listing seven December 2026 events with a pure-CSS category filter (All, Tech, Cultural, Sports, Workshops).
- **Registration modal** opened by any Register button, built with a CSS `:target` popup and native HTML5 validation for name, LPU registration number (8 digits), email, and event selection.
- **About page** with the mission and story, a showcase of LPU event venues, a `<details>`/`<summary>` FAQ, and an event submission and inquiry form.
- **Responsive layout** for desktop, tablet, and mobile.
- **Accessibility basics**: semantic HTML landmarks, visible focus styles, and support for reduced motion.

## Project Structure

```
campusconnect/
├── index.html    # Home page
├── events.html   # Events directory and registration modal
├── about.html    # About page, FAQ, and contact form
├── style.css     # Shared stylesheet for all pages
└── README.md     # This file
```

## Getting Started

No build step, package manager, or server is required.

1. Clone or download the repository:
   ```bash
   git clone https://github.com/<your-username>/campusconnect.git
   cd campusconnect
   ```
2. Open `index.html` in any modern web browser.

All pages link to the shared `style.css` with relative paths, so keep the four files in the same folder.

## Hosting on GitHub Pages

1. Push the repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` (or your default branch), and set the folder to `/ (root)`.
4. Save. The site will be published at `https://<your-username>.github.io/campusconnect/`.

## Technology

- HTML5 with semantic elements
- CSS3 with custom properties, Grid, Flexbox, transitions, and media queries
- Google Fonts (Bricolage Grotesque) with system-font fallbacks

No JavaScript is used anywhere in the project.

## Design Palette

| Role | Value |
|---|---|
| Primary accent (orange) | `#FF6600` |
| Dark accent (hover) | `#E55A00` |
| Soft accent tint | `#FFF5EE` |
| Featured gradient | `linear-gradient(135deg, #FF7A1A 0%, #FFB067 100%)` |
| Background | `#FFFFFF` |
| Primary text | `#1A1A1A` |
| Secondary text | `#666666` |
| Borders | `#EAEAEA` |
| Neutral surface | `#F3F3F3` |

All values are defined as CSS custom properties at the top of `style.css`, so you can change the theme in one place.

## Limitations

This is a front-end prototype. By design it has no backend, so:

- **Forms do not save or send data.** The registration and contact forms validate input in the browser and then show a confirmation message. Nothing is stored or emailed.
- **Event data is hard-coded** in `events.html` and `index.html`. Editing an event means changing the HTML directly.
- **Filtering and modals rely on the URL hash**, so the Back button and direct links to `#register` or `#list` behave as expected but do not persist any state.

To collect real registrations, connect the form `action` attributes to a form service (such as Formspree or Google Forms) or a server endpoint.

## Browser Support

Works in current versions of Chrome, Edge, Firefox, and Safari. The red invalid-field highlight uses the `:user-invalid` pseudo-class, which requires a recent browser; older browsers still show native validation messages.

## Contributing

Contributions are welcome. Please keep to the project's constraints: HTML and CSS only, with no JavaScript. Open an issue to discuss larger changes before submitting a pull request.

## License

Add a license of your choice here (for example, MIT). Until one is added, all rights are reserved by the author.

## Acknowledgements

Built for the Lovely Professional University community. CampusConnect is an independent student project and is not an official LPU website.
