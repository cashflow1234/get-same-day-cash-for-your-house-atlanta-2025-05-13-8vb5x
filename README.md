# USA Discount Property Landing Page - Maintenance Guide

This guide will help you maintain and customize the USA Discount Property landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
```html
<header class="fixed w-full bg-gray-900/95 backdrop-blur-sm z-50 border-b border-gray-800">
    <div class="text-xl font-bold text-white">USA Discount Property</div>
</header>
```
To update the company name:
1. Locate the `<div>` with class `text-xl font-bold text-white`
2. Replace "USA Discount Property" with your desired text
3. Adjust text size by changing `text-xl` to `text-lg` (smaller) or `text-2xl` (larger)

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-emerald-400">
    Get Same Day Cash For Your House Atlanta
</h1>
```
To modify the main headline:
1. Find the `<h1>` tag in the hero section
2. Update the text between the tags
3. The gradient effect is created by these classes:
   - `bg-gradient-to-r`: Right-direction gradient
   - `from-blue-400 to-emerald-400`: Color stops
   - `text-transparent bg-clip-text`: Makes text show gradient

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-700 rounded-xl p-8 hover:transform hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="text-emerald-400 mb-4">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Same Day Cash</h3>
    <p class="text-gray-300">Get your money immediately...</p>
</div>
```
To add or modify features:
1. Locate the features grid (`id="features"`)
2. Copy an existing feature card `<div>`
3. Update the:
   - Title in the `<h3>` tag
   - Description in the `<p>` tag
   - Icon SVG (if needed)

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```
To update navigation links:
1. Find the `<a>` tag you want to modify
2. Update the `href` attribute:
   - For same-page sections, use `#section-id`
   - For external links, use full URL (e.g., `https://example.com`)
   - For internal pages, use relative paths (e.g., `./about.html`)

### Call-to-Action Links
Current CTA button:
```html
<a href="https://form.jotform.com/250276622130043" class="inline-block bg-emerald-500 hover:bg-emerald-600 text-white font-semibold px-8 py-4 rounded-lg transform hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-emerald-500/25">
    Get Your Cash Offer Now
</a>
```
To update the form link:
1. Replace the JotForm URL with your new form URL
2. Keep the existing classes for consistent styling
3. Update button text if needed

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout on Mobile**
   - Check that all responsive classes (md:, lg:) are intact
   - Verify the viewport meta tag exists:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

2. **Missing Styles**
   - Confirm Tailwind CSS CDN is loading:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - Check for typos in class names

3. **Links Not Working**
   - Verify IDs match href attributes for internal links
   - Test external URLs in a browser
   - Ensure relative paths are correct for internal pages

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser dev tools

Remember to always test changes across different devices and browsers before deploying to production.