# All County Junk Removal Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the All County Junk Removal landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-gray-800">
    All County Junk <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#faq">FAQ</a> <!-- Update text here -->
</div>
```

### Hero Section
The main headline and subheading can be updated here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    <!-- Update subheading here -->
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout the page:
- Text sizes: `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-800`, `text-blue-600`
- Spacing: `px-6`, `py-4`, `mb-6`
- Responsive design: `md:text-5xl`, `lg:text-6xl`

To modify a style:
1. Find the element you want to change
2. Locate the class attribute
3. Add or replace Tailwind classes as needed

Example:
```html
<!-- Original -->
<div class="text-xl text-gray-600">

<!-- To make text larger and blue -->
<div class="text-2xl text-blue-600">
```

## Fixing Broken Links

### Current Link Structure
The page contains the following links:

1. Navigation Menu:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="tel:888-441-6653">Call Now</a>
```

2. Footer Links:
```html
<a href="#services">Services</a>
<a href="#faq">FAQ</a>
```

### Updating Links
To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text if needed

Example:
```html
<!-- Original -->
<a href="#services">Services</a>

<!-- Updated to link to services page -->
<a href="/services.html">Services</a>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#services" class="text-gray-400 hover:text-white transition-colors duration-300">Services</a></li>
        <li><a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
   - Check for `md:` and `lg:` prefixes in classes
   - Ensure the viewport meta tag is present
   - Test on different screen sizes

2. **Misaligned Elements**
   - Verify container classes are present: `container mx-auto px-6`
   - Check spacing classes (margin and padding)
   - Ensure grid classes are correct: `grid grid-cols-1 md:grid-cols-3`

3. **Link Issues**
   - Verify href attributes start with `/` for root-relative paths
   - Check for typos in file names
   - Ensure linked files exist in the correct directory

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct location
3. Test the page in multiple browsers
4. Ensure all Tailwind CSS classes are spelled correctly

Remember to always backup your files before making changes, and test your updates in a development environment first.