# Mystery Box Store SPA

A React-based Single Page Application for a mystery box store, designed as a Telegram Mini App.

## Project Structure

This project was generated using Figma Make and contains:

- **src/app**: Main application components
- **src/components**: Reusable UI components
- **src/context**: React context for state management
- **src/data**: Data files and configuration
- **src/styles**: CSS stylesheets

## Setup & Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Installation Steps

1. Clone the repository:
```bash
git clone https://github.com/sergeyphaeton-alt/mystery-box-spa.git
cd mystery-box-spa
```

2. Install dependencies:
```bash
npm install
```

## Development

Start the development server:
```bash
npm run dev
```

The app will run on `http://localhost:5173`

## Build for Production

Build the optimized production bundle:
```bash
npm run build
```

This generates a `dist/` folder with the compiled files.

## Deployment to Yandex Object Storage

### Prerequisites
- Yandex Cloud account
- AWS CLI or Yandex CLI configured

### Steps

1. Build the project:
```bash
npm run build
```

2. Upload the `dist/` folder contents to your Yandex Object Storage bucket:
```bash
aws s3 sync dist/ s3://mystery-box/ --endpoint-url https://storage.yandexcloud.net
```

3. Ensure your bucket is configured for website hosting:
   - Set index document: `index.html`
   - Set error document: `index.html` (for SPA routing)

4. Set bucket policy to allow public read access

5. Access your site at: `https://<bucket-name>.website.yandexcloud.net/`

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run linting

## Features

- React Router for client-side routing
- Shopping cart functionality
- Product catalog
- Responsive design
- Tailwind CSS styling
- Toast notifications with Sonner

## License

MIT
