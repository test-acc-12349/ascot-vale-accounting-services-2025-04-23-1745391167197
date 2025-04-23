# Ascot Vale Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Ascot Vale Accounting landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
The company name appears in the header navigation:
```html
<div class="text-2xl font-bold text-gray-800">
    Ascot Vale Accounting  <!-- Update company name here -->
</div>
```

#### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8">
    Ascot Vale accounting services  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Accounting excellence with a personal touch  <!-- Update tagline -->
</p>
```

#### Features Section
Each feature card contains:
```html
<h3 class="text-xl font-semibold mb-4 text-gray-900">
    Retirement Planning  <!-- Update feature title -->
</h3>
<p class="text-gray-600 leading-relaxed">
    Expert guidance for your retirement journey...  <!-- Update feature description -->
</p>
```

### Tailwind CSS Modifications

#### Understanding Responsive Classes
The page uses these breakpoints:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
<!-- text-4xl: Default size for mobile -->
<!-- md:text-5xl: Size for medium screens -->
<!-- lg:text-6xl: Size for large screens -->
```

#### Common Tailwind Classes Used
- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`
- Spacing: `px-6`, `py-4`, `mb-8`
- Flex layout: `flex`, `items-center`, `justify-between`

To modify a style, locate the relevant class and replace it with a new one from the same category.

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace the value with your desired link
3. For internal sections, use `#section-id`
4. For external pages, use the full URL

### Call-to-Action Links
Update the "Get Started" buttons:
```html
<a href="https://theaccountants.com" class="inline-block bg-blue-600...">
    Get Started Today
</a>
```
Replace `https://theaccountants.com` with your actual booking or contact page URL.

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Replace the `#` placeholder:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

2. Create matching HTML files:
- Create `privacy.html` in the same directory
- Create `terms.html` in the same directory
- Use the same styling classes for consistency

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match the href values
- Check for typos in the href attributes
- Verify that section IDs are unique

2. **Responsive Design Issues**
- Check that you're using the correct breakpoint prefixes (`md:`, `lg:`)
- Maintain the responsive class pattern when updating
- Test on different screen sizes after changes

3. **Style Inconsistencies**
- Keep color classes consistent (e.g., `text-gray-900`, `bg-blue-600`)
- Maintain spacing patterns using similar padding/margin classes
- Use the existing class structure as a template for new elements

### Need Help?
- Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check the HTML structure before making changes
- Make one change at a time and test thoroughly
- Keep a backup of the original code

Remember to test all changes across different devices and browsers to ensure consistency in appearance and functionality.