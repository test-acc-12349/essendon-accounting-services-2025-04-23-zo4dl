# Essendon Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- CTA Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located in the header section -->
<a href="/" class="text-xl font-bold text-white">
    Essendon<span class="text-blue-500">.</span>
</a>
```
To change the company name, modify the text "Essendon" directly. The blue dot can be removed by deleting the `<span>` element.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8">
    Essendon accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-400 mb-12">
    Trusted advisors for your financial future
</p>
```
- Change the main heading by updating the text inside the `<h1>` tags
- Modify the subheading by updating the text inside the `<p>` tags

### Understanding Tailwind Classes

#### Responsive Design Classes
In this landing page, responsive classes follow this pattern:
- Default (mobile): `text-4xl`
- Medium screens (md): `md:text-5xl`
- Large screens (lg): `lg:text-6xl`

Example:
```html
<!-- This text is:
     - 2xl on mobile (text-2xl)
     - 3xl on medium screens (md:text-3xl)
     - 4xl on large screens (lg:text-4xl) -->
<h2 class="text-2xl md:text-3xl lg:text-4xl">
```

#### Common Styling Classes
- Text colors: `text-white`, `text-gray-400`, `text-blue-500`
- Background colors: `bg-gray-900`, `bg-blue-600`
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Hover effects: `hover:bg-blue-700`, `hover:text-white`

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
    <a href="https://theaccountants.com" class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-full">
        Get Started
    </a>
</div>
```

To update links:
1. Locate the `href` attribute in the `<a>` tag
2. Replace with your new URL:
   - For internal sections, use `#section-name`
   - For external links, use the full URL (e.g., `https://example.com`)

### Call-to-Action (CTA) Links
There are multiple CTA buttons throughout the page. Update all instances of:
```html
<a href="https://theaccountants.com" class="inline-flex items-center...">
```
Replace `https://theaccountants.com` with your desired URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check that href values start with `#` for internal links
   - Verify that external URLs include `https://`
   - Ensure section IDs match their corresponding links

2. **Responsive Design Issues**
   - Make sure you're not removing responsive classes (md: and lg: prefixes)
   - Test on different screen sizes using browser dev tools
   - Keep the container classes intact: `container mx-auto px-4 sm:px-6 lg:px-8`

3. **Styling Problems**
   - Don't remove essential Tailwind classes without replacement
   - Maintain the structure of utility classes
   - Keep hover states (`hover:`) for interactive elements

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify all changes against the original code
3. Test in multiple browsers
4. Ensure all required CSS and JavaScript files are properly linked

Remember to always backup your code before making significant changes!