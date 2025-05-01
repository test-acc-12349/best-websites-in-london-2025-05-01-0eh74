# LondonWeb Landing Page - Maintenance Guide

This guide will help you maintain and customize the LondonWeb landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Locate this line in the header:
```html
<a href="/" class="text-2xl font-bold text-gray-800">London<span class="text-blue-600">Web</span></a>
```
- Change "London" and "Web" to your desired text
- Keep the `<span>` tags to maintain the blue color on the second word

2. **Navigation Menu Items**: Find these lines:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <!-- ... -->
</div>
```
- Update text between `>` and `</a>` for each menu item
- Keep the classes to maintain styling and hover effects

### Hero Section
Located right after the header:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In London
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```
- Update heading and subheading text as needed
- Don't remove the responsive classes (`text-4xl md:text-5xl lg:text-6xl`)
- These ensure proper sizing on different devices

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-xl`, `px-6`) control size
- `md:` and `lg:` prefixes apply styles at specific screen sizes
- Color classes use format: `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing classes use format: `m-{size}` for margin, `p-{size}` for padding

## Managing Links

### Current Link Locations

1. **Navigation Menu Links**:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
- These are internal links to page sections
- The `#` symbol links to element IDs on the same page

2. **Call-to-Action Buttons**:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600...">
```
- Replace `https://sigmaseo.io` with your desired URL
- Always include `https://` for external links

3. **Footer Links**:
```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <!-- ... -->
</ul>
```
- Update these to match your navigation menu changes
- Keep the same format for consistency

### Updating Links Step-by-Step

1. For internal section links:
   - Ensure the `href` matches the `id` of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. For external links:
   - Replace placeholder URLs with actual websites
   - Always test links after updating
   - Include full URLs starting with `https://`

## Adding Privacy and Terms Pages

### Step 1: Locate Footer Links
Find this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update Link Paths
Replace the `#` with proper file paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Create New Pages
1. Create `privacy.html` and `terms.html` in your website folder
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between them

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Styling Problems**
   - Don't remove classes containing `md:` or `lg:` prefixes
   - Keep `transition`, `duration`, and `hover` classes together
   - Maintain the same class structure when copying elements

3. **Layout Issues**
   - Keep the `container mx-auto px-6` classes on main sections
   - Don't remove `grid` classes from multi-column layouts
   - Preserve responsive classes to maintain mobile compatibility

Need more help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).