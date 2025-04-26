# Landing Page Maintenance Guide

This guide will help you maintain and customize the Ayla Doeken landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name. To update:

1. **Brand Name**
```html
<!-- Located at the top of the page -->
<a href="#" class="text-2xl font-bold text-gray-800">
    Ayla Doeken  <!-- Change this text to update the brand name -->
</a>
```

2. **Navigation Menu Items**
```html
<div class="hidden lg:flex space-x-8">
    <!-- Modify these link texts as needed -->
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Voordelen</a>
```

### Hero Section
The main welcome section at the top:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold">
    Schrijf Alles In Het Nederlands  <!-- Main headline -->
    <span class="text-blue-600">Ayla Doeken</span>  <!-- Sub-headline -->
</h1>
```

#### Tailwind CSS Class Guide
- `text-4xl`: Large text (mobile)
- `sm:text-5xl`: Larger text on small screens
- `lg:text-6xl`: Largest text on large screens
- `font-extrabold`: Very bold text
- `text-blue-600`: Blue colored text

### Features Section
To modify feature cards:

```html
<div class="bg-white p-8 rounded-2xl shadow-lg">
    <div class="text-blue-600 text-4xl mb-4">🚀</div>  <!-- Emoji icon -->
    <h3 class="text-xl font-bold mb-4">Onweerstaanbare Content</h3>  <!-- Feature title -->
    <p class="text-gray-600">Leer hoe je teksten schrijft...</p>  <!-- Feature description -->
</div>
```

## Managing Links

### Navigation Links
All internal navigation links use anchor tags with hashtags (#):

```html
<!-- Current navigation links -->
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- To update, modify the href attribute -->
<a href="#new-section">New Section</a>
```

### Call-to-Action Buttons
There are two main CTA buttons:

```html
<!-- Hero section button -->
<a href="https://amzn.to/44FEZmc" class="inline-block bg-blue-600 text-white">
    Begin Nu Direct! →
</a>

<!-- Bottom section button -->
<a href="https://amzn.to/44FEZmc" class="inline-block bg-white text-blue-600">
    Claim Nu Je Voordeel →
</a>
```

To update:
1. Replace `https://amzn.to/44FEZmc` with your desired URL
2. Modify button text between the `<a>` tags

## Adding Privacy and Terms Pages

### Footer Links
Current placeholder links in the footer:

```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```

To link to actual pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match href attributes
- Check for typos in IDs
- Verify that sections have the correct ID attribute:
```html
<section id="features">  <!-- This ID must match the href="#features" -->
```

2. **Responsive Design Issues**
- Check that you're maintaining the responsive classes:
  - `sm:` prefix for small screens
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
```html
<!-- Example of responsive classes -->
<h1 class="text-4xl sm:text-5xl lg:text-6xl">
```

3. **Style Changes Not Working**
- Verify Tailwind CSS is properly loaded
- Check for typos in class names
- Ensure classes are space-separated

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct location
3. Ensure all links use the correct relative paths
4. Confirm all HTML tags are properly closed

Remember to test all changes across different screen sizes using your browser's developer tools.