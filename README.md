# Linda Plants Store

An online plant store built with Astro.js, Tailwind CSS, and TypeScript. Integrated with Shopify Storefront API for product catalog, inventory management, and checkout.

## Features

- 🌿 Dynamic plant catalog from Shopify Storefront API
- 🛒 Full shopping cart and checkout experience
- 📱 Fully responsive design for mobile and desktop
- 🔍 Product search, filtering, and sorting
- 🎨 Automatic light/dark mode theme switcher
- ⚡ Fast page loads with Astro's static generation
- 🔐 User authentication and account management
- 🏷️ Product categories, tags, and variants
- �� Secure checkout through Shopify
- ♿ SEO optimized with sitemap and meta tags

## Tech Stack

- **Framework**: Astro 5.16+
- **Styling**: Tailwind CSS 4.1+
- **Language**: TypeScript 5.9+
- **E-commerce**: Shopify Storefront API (GraphQL)
- **Runtime**: Node.js v22.20+
- **Package Manager**: npm v10.2+
- **Deployment**: Netlify (pre-configured)

## Getting Started

### Prerequisites

- Node.js 22.20 or higher
- npm 10.2 or higher
- Shopify Partner account with development store

### Setup Shopify

1. Create a Shopify Partner account and development store
2. Add products to your store (or import from `/public/products.csv`)
3. Create an app in your Shopify admin:
   - Go to Settings → Apps and sales channels → Develop apps
   - Create a new app
   - Configure Storefront API scopes (select all)
   - Install the app and get your credentials

4. Copy `.env.example` to `.env` and add your credentials:
```bash
PUBLIC_SHOPIFY_API_SECRET_KEY="your-api-key"
PUBLIC_SHOPIFY_STOREFRONT_ACCESS_TOKEN="your-access-token"
PUBLIC_SHOPIFY_STORE_DOMAIN="your-store.myshopify.com"
```

### Installation

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

The dev server will run at `http://localhost:4321`

### Configure Collections

Edit `/src/config/config.json` to customize:
- Site title and branding
- Currency settings
- Shopify collection names for hero slider and featured products
- Theme colors and fonts

Create corresponding collections in your Shopify admin that match the names in the config file.

## Project Structure

```
/
├── public/              # Static assets
├── src/
│   ├── components/      # Reusable Astro components
│   ├── config/          # Configuration files
│   ├── content/         # Markdown content (About, Contact, etc.)
│   ├── layouts/         # Page layouts and partials
│   ├── lib/             # Utility functions and Shopify API
│   ├── pages/           # Astro pages and API routes
│   ├── styles/          # Global CSS and Tailwind config
│   └── types/           # TypeScript type definitions
├── astro.config.mjs     # Astro configuration
├── tailwind.config.js   # Tailwind configuration
└── tsconfig.json        # TypeScript configuration
```

## Key Pages

- `/` - Homepage with hero slider and featured products
- `/products` - Product listing page with filters
- `/products/[slug]` - Individual product pages
- `/about` - About the store
- `/contact` - Contact form
- `/login` - Customer login
- `/sign-up` - Customer registration

## Customization

### Branding
Update `/src/config/config.json` with your store name, logo, and metadata

### Content
Edit markdown files in `/src/content/` for About, Contact, and other pages

### Styling
Modify `/src/config/theme.json` for colors and typography
Custom CSS in `/src/styles/`

### Products
Managed entirely through your Shopify admin dashboard

## Deployment

Pre-configured for Netlify deployment:

```bash
# Deploy to Netlify
netlify deploy --prod
```

Or connect your GitHub repository to Netlify for automatic deployments.

## Environment Variables

Required environment variables:
- `PUBLIC_SHOPIFY_API_SECRET_KEY` - Your Shopify app API key
- `PUBLIC_SHOPIFY_STOREFRONT_ACCESS_TOKEN` - Storefront access token
- `PUBLIC_SHOPIFY_STORE_DOMAIN` - Your store domain (*.myshopify.com)

## License

MIT License - see LICENSE file for details

## Support

For questions about Shopify integration, refer to the [Shopify Storefront API documentation](https://shopify.dev/api/storefront).

For Astro-specific questions, visit the [Astro documentation](https://docs.astro.build).
