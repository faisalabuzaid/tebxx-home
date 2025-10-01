# TebbX Landing Page

A professional, enterprise-level landing page for TebbX clinic management system.

## 🚀 Features

- **Minimal Black & White Design**: Clean, professional aesthetic with pure black and white
- **SVG Logo**: Crisp, scalable logo from your brand assets
- **Responsive**: Mobile-first design that works on all devices
- **Fast Loading**: Optimized for performance
- **SEO Friendly**: Proper meta tags and semantic HTML
- **Conversion Optimized**: Clear CTAs and waitlist signup form
- **Simplified Navigation**: Minimal header focused on conversion

## 📋 Sections

1. **Hero Section**: Eye-catching headline with CTA buttons
2. **Features**: 6 key features of the clinic management system
3. **Benefits**: Why healthcare professionals should choose TebbX
4. **Pricing**: Three pricing tiers (Starter, Professional, Enterprise)
5. **Waitlist Form**: Capture early adopters
6. **Footer**: Links and social media connections

## 🛠️ Technologies Used

- HTML5
- Tailwind CSS (via CDN)
- Font Awesome Icons
- Vanilla JavaScript

## 📦 Deployment to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it something like `tebbx-landing` or `clinic-management-landing`
3. Make it public (required for free GitHub Pages)
4. Don't initialize with README (we already have one)

### Step 2: Push Your Code

```bash
cd /home/faisal/private/projects/tebbx/home

# Initialize git repository
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: TebbX landing page"

# Add your GitHub repository as remote (replace with your actual repo URL)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select **main** branch
5. Select **/ (root)** folder
6. Click **Save**
7. GitHub will provide you with a URL like: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

Your site should be live in 1-2 minutes!

## 🌐 Connecting Your GoDaddy Domain

### Step 1: Create CNAME File (Already Done)

The `CNAME` file in the root contains your custom domain. Update it with your actual domain:

```
yourdomain.com
```

or

```
www.yourdomain.com
```

### Step 2: Configure DNS in GoDaddy

1. Log in to your [GoDaddy account](https://www.godaddy.com)
2. Go to **My Products** → **DNS**
3. Find your domain and click **DNS**

#### For Root Domain (example.com):

Add these **A Records**:

```
Type: A
Name: @
Value: 185.199.108.153
TTL: 600 seconds

Type: A
Name: @
Value: 185.199.109.153
TTL: 600 seconds

Type: A
Name: @
Value: 185.199.110.153
TTL: 600 seconds

Type: A
Name: @
Value: 185.199.111.153
TTL: 600 seconds
```

#### For Subdomain (www.example.com):

Add a **CNAME Record**:

```
Type: CNAME
Name: www
Value: YOUR_USERNAME.github.io
TTL: 1 Hour
```

### Step 3: Update CNAME File

1. Edit the `CNAME` file in your repository
2. Add your domain (e.g., `tebbx.com` or `www.tebbx.com`)
3. Commit and push:

```bash
git add CNAME
git commit -m "Add custom domain"
git push
```

### Step 4: Configure Custom Domain in GitHub

1. Go to repository **Settings** → **Pages**
2. Under **Custom domain**, enter your domain
3. Click **Save**
4. Wait for DNS check to complete
5. Enable **Enforce HTTPS** (recommended)

### Step 5: Wait for DNS Propagation

- DNS changes can take 24-48 hours to propagate globally
- Usually takes 10-30 minutes for most users
- Check status at: https://dnschecker.org

## 🔧 Customization

### Update Domain in CNAME

Edit `/CNAME` file with your actual domain name.

### Customize Content

Edit `index.html` to update:
- Company information
- Feature descriptions
- Pricing details
- Contact information
- Social media links

### Update Images

Replace the Unsplash image URLs with your own:
- Hero section image
- Benefits section image

### Form Integration

The waitlist form currently logs to console. Integrate with:

**Option 1: Formspree** (Easiest)
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

**Option 2: Google Forms** (Free)
- Create a Google Form
- Use form URL as action

**Option 3: Mailchimp** (Email Marketing)
- Embed Mailchimp signup form

**Option 4: Custom Backend**
- Point form to your API endpoint

### Update Colors

The current design uses a minimal black and white palette:

**Current Colors:**
- Rich Black: `#0a0a0a` (primary, buttons, text - softer than pure black)
- White: `#ffffff` (backgrounds, button hover)
- Light Gray: `#fafafa` (section backgrounds)
- Gray borders: `#e5e5e5`, `#d1d5db`
- Gray text: `#6b7280`, `#9ca3af`

To add color:
1. Update the `.btn-primary` and `.icon-box` classes in `index.html`
2. Replace `#000000` with your brand color
3. Adjust hover states accordingly

Or use Tailwind's color utilities:
- `bg-black` → `bg-blue-600`, `bg-purple-600`, etc.
- `border-black` → `border-blue-600`, etc.

## 🎨 Design Features

- **Minimal Black & White**: Pure #000000 and #FFFFFF color palette
- **Clean Typography**: Bold, readable Inter font
- **Subtle Borders**: Delicate #e5e5e5 borders for separation
- **Smooth Transitions**: Hover effects on buttons and cards
- **Rounded Corners**: Modern border-radius for softness
- **SVG Icons**: Inline SVG checkmarks and elements
- **Centered Layouts**: Balanced, symmetrical design
- **Negative Space**: Generous whitespace for breathing room

## 📊 Analytics (Optional)

Add Google Analytics by inserting this before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔒 Security & Performance

- HTTPS enforced via GitHub Pages
- No sensitive data stored client-side
- Optimized images from CDN
- Minimal JavaScript for fast loading

## 📞 Support

For questions or issues:
- Email: support@tebbx.com
- Website: https://tebbx.com

## 📄 License

© 2025 TebbX. All rights reserved.

---

Built with ❤️ for healthcare professionals

