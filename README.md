# Potomac Landing Page - Maintenance Guide

This guide will help you maintain and customize the Potomac landing page for frameless shower doors. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold tracking-tighter text-white hover:text-purple-400">
    Potomac <!-- Change this text to update company name -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8">
    Frameless shower doors - sleek & modern <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Experience luxury and elegance... <!-- Subheading text -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Sets text size (increases with screen size)
- `md:text-6xl`: Applies different text size on medium screens
- `font-bold`: Makes text bold
- `mb-8`: Adds margin bottom (spacing)
- `text-gray-300`: Sets text color to light gray

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes while maintaining responsive classes (those starting with `md:` or `lg:`)

## Managing Links

### Current Link Locations
1. Navigation Menu:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Button:
```html
<a href="http://www.customeuroglass.com" class="inline-block bg-gradient-to-r...">
    Explore Our Collection
</a>
```

3. Footer Links:
```html
<a href="mailto:ts@customeuroglass.com">ts@customeuroglass.com</a>
<a href="http://www.customeuroglass.com">Website</a>
```

### Updating Links
1. For internal links (same page sections):
   - Use `#section-name` format
   - Ensure the section ID matches exactly
   ```html
   <a href="#features">Features</a>
   <section id="features">...</section>
   ```

2. For external links:
   - Use complete URLs starting with `http://` or `https://`
   ```html
   <a href="https://your-new-website.com">Website</a>
   ```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's "Links" section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <a href="http://www.customeuroglass.com" class="text-gray-400 hover:text-white transition-colors duration-300 block">
        Website
    </a>
    <!-- Add these new links -->
    <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300 block">
        Privacy Policy
    </a>
    <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300 block">
        Terms of Service
    </a>
</div>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   ```html
   <!-- Correct -->
   <a href="#features">
   <section id="features">

   <!-- Wrong -->
   <a href="#Features">
   <section id="features">
   ```

2. **Responsive Design Issues**
   - Keep responsive classes (`md:`, `lg:`) when updating
   - Test on different screen sizes
   ```html
   <!-- Maintain responsive classes -->
   <h1 class="text-4xl md:text-6xl lg:text-7xl">
   ```

3. **Styling Inconsistencies**
   - Copy existing class combinations for similar elements
   - Example for new buttons:
   ```html
   class="inline-block bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold px-8 py-4 rounded-lg transform hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-purple-500/25"
   ```

### Need Help?
- Double-check class names against Tailwind CSS documentation
- Verify all links start with either `#`, `/`, or `http://`
- Test all changes in multiple browsers
- Use browser developer tools (F12) to inspect elements

Remember to always backup your files before making changes, and test thoroughly on different devices and browsers.