# Portfolio

A modern, responsive portfolio website built with Nuxt 3 and Nuxt UI.

## Features

- 🎨 Beautiful, responsive design with dark mode support
- ⚡ Fast and optimized with Nuxt 3
- 🎯 Portfolio sections: Home, About, Skills, Projects, Contact
- 🔧 Built with Nuxt UI components
- 📱 Mobile-first approach
- 🎭 Professional UI with Tailwind CSS

## Setup

Install dependencies:

```bash
pnpm install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
pnpm dev
```

## Production

Build the application for production:

```bash
pnpm build
```

Preview production build:

```bash
pnpm preview
```

## Customization

To customize the portfolio for your own use:

1. Update personal information in `app/pages/index.vue`:
   - Replace "Your Name" with your actual name
   - Update the hero description
   - Modify the About section content

2. Update projects in `app/pages/index.vue`:
   - Replace placeholder project data with your actual projects
   - Add project images to `/public/images/`
   - Update project links and tags

3. Update skills in `app/pages/index.vue`:
   - Modify the skills array with your technologies

4. Update contact information:
   - Replace email, GitHub, and LinkedIn URLs
   - Update social links in `app/app.vue`

5. Update SEO metadata in `app/app.vue`:
   - Change the title and description

Note: Project images are currently using placeholders. Replace the image paths with your actual project screenshots.

## Tech Stack

- [Nuxt 3](https://nuxt.com/) - Vue.js Framework
- [Nuxt UI](https://ui.nuxt.com/) - UI Component Library
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [TypeScript](https://www.typescriptlang.org/) - Type Safety

## License

See [LICENSE](LICENSE) file for details.
