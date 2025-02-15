# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>

<!-- Navigation Menu Items -->
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional menu items -->
</div>
```

To change:
1. Logo text: Replace "TWD" with your desired text
2. Menu items: Modify the text between `<a>` tags
3. Colors: Update `text-blue-600` to other Tailwind colors (e.g., `text-red-600`)

### Hero Section
The main banner section contains:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-white mb-8">Best Websites In Texas</p>
```

To modify:
1. Main heading: Replace text between `<h1>` tags
2. Subheading: Update text between `<p>` tags
3. Size adjustment: Modify text sizes using Tailwind classes
   - `text-4xl` = desktop size
   - `md:text-6xl` = mobile size

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl">
    <i class="fas fa-server text-4xl text-blue-600 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```

To modify:
1. Icon: Change `fa-server` to any [Font Awesome](https://fontawesome.com/icons) icon
2. Title: Update text in `<h3>` tags
3. Description: Modify text in `<p>` tags

## Managing Links

### Navigation Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links: Keep the `#` prefix for same-page sections
2. External links: Replace with full URLs
   ```html
   <a href="https://example.com">External Link</a>
   ```

### Call-to-Action Buttons
Located in hero and contact sections:

```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Start Your Project
</a>
```

To modify:
1. Replace `https://twd.com` with your destination URL
2. Update button text between `<a>` tags

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Link back to home:
   ```html
   <a href="index.html">Return to Home</a>
   ```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   ```html
   <section id="features">  <!-- ID here -->
   <a href="#features">     <!-- Must match exactly -->
   ```

2. **Responsive Design Issues**
   - Check mobile classes (prefixed with `md:`)
   - Test different screen sizes
   - Common responsive classes used:
     ```html
     text-4xl md:text-6xl  <!-- Mobile: 4xl, Desktop: 6xl -->
     flex-col md:flex-row  <!-- Mobile: Column, Desktop: Row -->
     ```

3. **Icon Not Showing**
   - Verify Font Awesome CSS is loaded
   - Check icon class names
   - Example fix:
     ```html
     <i class="fas fa-server"></i>  <!-- Correct -->
     <i class="fa fa-server"></i>   <!-- Incorrect -->
     ```

### Need More Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check Font Awesome [icon reference](https://fontawesome.com/icons)
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test changes across different devices and browsers before deploying to production.