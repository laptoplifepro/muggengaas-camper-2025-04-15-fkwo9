# Muggengaas Camper Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Muggengaas Camper landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<a href="#" class="text-2xl font-bold text-gray-900">Muggengaas Camper</a>
```
- Replace "Muggengaas Camper" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight mb-8">
    Muggengaas Camper
</h1>
<p class="text-xl sm:text-2xl text-gray-600 mb-10">
    Professional mosquito protection solutions for your camper
</p>
```
- Update heading and subheading text as needed
- Maintain responsive classes (sm:, lg:) for different screen sizes

### Features Section
To add or modify feature cards:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300 transform hover:scale-105">
    <div class="text-blue-600 mb-4">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold text-gray-900 mb-2">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```
- Copy entire `div` block to add new features
- Maintain grid layout using `grid-cols-1 md:grid-cols-2 lg:grid-cols-3`

### Tailwind CSS Class Guide
Common classes used:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-900`, `text-blue-600`, `bg-white`
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Hover effects: `hover:text-gray-900`, `hover:bg-gray-100`

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden lg:flex lg:items-center lg:space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update links:
1. Internal links (same page):
   - Use `#section-name` format
   - Ensure section IDs match exactly
   
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://your-site.com/page"`

### Get Started Button
```html
<a href="https://sites.google.com/view/muggengaascamper" class="inline-flex items-center justify-center px-4 py-2 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-blue-600 hover:bg-blue-700">
    Get Started
</a>
```
- Update `href` attribute with your desired URL
- Maintain button styling classes for consistent appearance

## Adding Privacy and Terms Pages

### Footer Links Setup
Current footer link structure:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - Example: `href="#features"` must match `id="features"`
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Maintain responsive classes (sm:, md:, lg:)
   - Test on different screen sizes
   - Don't remove container classes: `container mx-auto px-4`

3. **Style Inconsistencies**
   - Keep consistent color classes (text-gray-900, text-blue-600)
   - Maintain spacing patterns (p-8, mb-4)
   - Copy existing component styles for new elements

### Need Help?
- Review Tailwind CSS documentation for class references
- Check browser developer tools (F12) for styling issues
- Ensure all links begin with either `#` (internal) or `http`/`https` (external)

Remember to test all changes across different devices and browsers before publishing updates.