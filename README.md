# RocketReviews.ai Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the RocketReviews.ai landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the brand name and registration button. To modify:

```html
<!-- Located at the top of the page -->
<div class="text-2xl font-bold">
    RocketReviews.ai  <!-- Change brand name here -->
</div>
<button class="bg-gradient-to-r from-blue-600 to-purple-600">
    Register Now      <!-- Change button text here -->
</button>
```

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
    5-Star Workshop: Use AI to Skyrocket Reviews <!-- Edit main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    How to Get More Reviews & Rank Higher <!-- Edit subheading -->
</p>
```

### Modifying Tailwind Classes
To adjust styling, modify the Tailwind classes. Common adjustments:

- Text size: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-blue-600`, `bg-purple-600`, etc.
- Spacing: `p-4` (padding), `m-4` (margin), `gap-4` (grid gap)
- Responsive design: Add `md:` or `lg:` prefix for different screen sizes

Example:
```html
<!-- Original -->
<div class="text-xl md:text-2xl text-gray-600">

<!-- Make text larger -->
<div class="text-2xl md:text-3xl text-gray-600">
```

## Managing Links

### Identifying Current Links
The page contains several placeholder links that need updating:

1. Main CTA Button:
```html
<a href="www.Eventbrite.com" class="inline-block">
    Secure Your Spot Now
</a>
```

2. Footer Links:
```html
<ul class="space-y-2">
    <li><a href="#">About Us</a></li>    <!-- Update href -->
    <li><a href="#">Features</a></li>    <!-- Update href -->
    <li><a href="#">Pricing</a></li>     <!-- Update href -->
</ul>
```

### Updating Links
To update any link:

1. Locate the `<a>` tag
2. Replace the `href="#"` or existing URL with your new URL
3. Ensure external links include `https://`

Example:
```html
<!-- Incorrect -->
<a href="www.Eventbrite.com">

<!-- Correct -->
<a href="https://www.eventbrite.com/your-event-page">
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:

```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating New Pages
1. Create two new files in your project folder:
   - `privacy.html`
   - `terms.html`

2. Copy this basic template for each:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - RocketReviews.ai</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body class="font-['Inter'] antialiased">
    <!-- Add your content here -->
</body>
</html>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for proper `https://` prefix
   - Verify file paths for internal links
   - Test all links after updating

2. **Styling Issues**
   - Ensure Tailwind CDN is loading
   - Check for typos in class names
   - Verify responsive classes use correct breakpoints (`md:`, `lg:`)

3. **Layout Problems**
   - Check container classes: `container mx-auto px-6`
   - Verify grid classes: `grid grid-cols-1 md:grid-cols-3`
   - Ensure proper nesting of elements

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct location
3. Ensure all HTML tags are properly closed
4. Compare your changes against the original code

Remember to always test your changes across different devices and screen sizes to ensure responsive design remains intact.