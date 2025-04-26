# Knuffel Ring Landing Page - Maintenance Guide

This guide will help you maintain and customize the Knuffel Ring landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Knuffel Ring  <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden lg:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

### Hero Section
The main banner section contains:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Koop Knuffel Ring Met Korting  <!-- Update this heading -->
</h1>
```

2. **Subheading:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    🔥 Nog maar enkele stuks beschikbaar!  <!-- Update this text -->
</p>
```

### Tailwind CSS Class Guide
Common classes used and their meanings:

- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[size]`: Adds margin bottom (4, 8, 12, etc.)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `hover:scale-105`: Enlarges element on hover
- `transition-colors`: Smooths color transitions

## Managing Links

### Navigation Links
All internal navigation links use section IDs:

```html
<!-- Current internal links -->
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- To update, match the href with your section ID -->
<section id="features">  <!-- This ID must match the href above -->
```

### Call-to-Action Links
Update the product link in two locations:

```html
<!-- Hero section CTA -->
<a href="https://amzn.to/42MY4QH" class="inline-block bg-gradient-to-r...">
    Bestel Nu Met Korting
</a>

<!-- Bottom CTA section -->
<a href="https://amzn.to/42MY4QH" class="inline-block bg-white...">
    Bestel Nu Met Korting
</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Files
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:

```html
<ul class="space-y-2 text-gray-400">
    <!-- Before -->
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>

    <!-- After -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Keep the Tailwind responsive prefixes (`md:`, `lg:`)
   - Test on multiple screen sizes
   - Don't remove the viewport meta tag

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

### Need Help?
1. Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
2. Validate your HTML at [W3C Validator](https://validator.w3.org/)
3. Test all links before deploying changes

Remember to always make a backup of your files before making significant changes!