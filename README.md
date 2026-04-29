# HAUS — E-commerce Website

A minimalist home living e-commerce website built with pure HTML, CSS, and JavaScript.

## 🚀 Quick Start

```bash
# Open in browser
open index.html
```

## 📁 Project Structure

```
ecommerce-site/
├── index.html          # Homepage
├── product.html         # Product detail page
├── README.md           # This file
└── images/             # Product images (add your own)
```

## 🚢 Deploy to Netlify (Recommended)

### Option 1: Drag & Drop
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the `ecommerce-site` folder to the deploy area
3. Done! Get your live URL instantly

### Option 2: GitHub Integration
```bash
# 1. Create a new GitHub repo
git init
git add .
git commit -m "Initial commit"

# 2. Push to GitHub
git remote add origin https://github.com/YOUR_USERNAME/haus-ecommerce.git
git push -u origin main

# 3. Connect to Netlify
# - Go to app.netlify.com
# - Click "Add new site" > "Import an existing project"
# - Select your GitHub repo
# - Deploy settings:
#   • Build command: (leave empty)
#   • Publish directory: .
# - Click "Deploy site"
```

### Option 3: Netlify CLI
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy (from ecommerce-site folder)
netlify deploy --prod
```

## 🚢 Deploy to Vercel

### Option 1: Drag & Drop
1. Go to [vercel.com](https://vercel.com)
2. New Project > Import
3. Drag the `ecommerce-site` folder
4. Deploy!

### Option 2: Vercel CLI
```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel --prod
```

### Option 3: GitHub Integration
1. Push to GitHub
2. Go to [vercel.com](https://vercel.com)
3. New Project > Import from GitHub
4. Select repo
5. Framework Preset: "Other"
6. Deploy!

## 🌐 Custom Domain

### Netlify
1. Site Settings > Domain Management
2. Add custom domain
3. Configure DNS:
   ```
   Type: CNAME
   Name: www (or @)
   Value: YOUR-SITE.netlify.app
   ```

### Vercel
1. Settings > Domains
2. Add custom domain
3. Configure DNS:
   ```
   Type: CNAME
   Name: www
   Value: cname.vercel-dns.com
   
   Type: A
   Name: @
   Value: 76.76.21.21
   ```

## 🔧 Configuration

### Update Site Info
Edit the following files:
- `index.html` — Logo, hero text, products, footer
- `product.html` — Product details, images

### Change Brand Name
Search and replace "HAUS" with your brand name in both files.

### Update Colors
Edit CSS variables in `<style>` section:
```css
:root {
    --bg: #FAFAF8;           /* Background */
    --text-primary: #1A1A1A; /* Main text */
    --accent: #8B7355;       /* Accent color */
}
```

## 💳 Payment Integration

### Stripe (Recommended)
```html
<!-- Add Stripe JS -->
<script src="https://js.stripe.com/v3/"></script>
```
- Create Stripe account
- Get publishable key
- Build checkout flow

### LemonSqueezy (Simpler)
```html
<!-- Add LemonSqueezy overlay checkout -->
<script src="https://app.lemonsqueezy.com/js/lemon.js" defer></script>
```

### Shopify Buy Button
1. Create Shopify store
2. Sales Channels > Buy Button
3. Generate embed code
4. Add to your site

## 📊 Analytics

### Google Analytics 4
```html
<!-- Add before </head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Fathom (Privacy-friendly)
```html
<script src="https://cdn.usefathom.com/script.js" site="YOUR-SITE-ID" defer></script>
```

## 🔍 SEO

Update `<title>` and add meta tags:
```html
<head>
    <title>Your Product Name — Brand</title>
    <meta name="description" content="Your product description here">
    <meta property="og:title" content="Your Product Name">
    <meta property="og:description" content="Your product description">
    <meta property="og:image" content="https://your-site.com/image.jpg">
    <meta property="og:url" content="https://your-domain.com">
    <link rel="canonical" href="https://your-domain.com">
</head>
```

## 🛠 Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Custom properties, Grid, Flexbox
- **JavaScript** — Vanilla ES6+
- **No build step** — Pure static files
- **Fonts** — Google Fonts (Outfit, DM Sans)
- **Images** — Unsplash (placeholder)

## 📱 Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 📄 License

MIT — Use freely for personal or commercial projects.
