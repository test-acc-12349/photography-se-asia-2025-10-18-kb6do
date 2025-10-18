# Photography SE Asia Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the Photography SE Asia landing page. Whether you're updating text, fixing links, or adding new pages, you'll find step-by-step instructions tailored to this specific landing page.

---

## Table of Contents

1. [Quick Start Guide](#quick-start-guide)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Working with Tailwind CSS Classes](#working-with-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Customizing Colors and Styling](#customizing-colors-and-styling)
8. [Responsive Design Tips](#responsive-design-tips)
9. [Troubleshooting Common Issues](#troubleshooting-common-issues)

---

## Quick Start Guide

### What You Need to Get Started

- **A text editor** - We recommend free options like:
  - [Visual Studio Code](https://code.visualstudio.com/) (most popular)
  - [Notepad++](https://notepad-plus-plus.org/)
  - Even basic Notepad will work

- **Your HTML file** - Save the index.html file to your computer

- **A web browser** - To preview changes (Chrome, Firefox, Safari, or Edge)

### How to Edit and Preview

1. **Open the file**: Right-click on `index.html` → Select "Open with" → Choose your text editor

2. **Make changes**: Edit the text in your editor

3. **Save changes**: Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)

4. **Preview**: Double-click the `index.html` file to open it in your browser, or right-click → "Open with" → Your browser

5. **Refresh to see updates**: After saving changes, press `F5` or `Ctrl+R` to refresh the browser

---

## Understanding the Page Structure

This landing page is organized into distinct sections. Understanding this structure makes editing much easier.

### Main Page Sections (in order from top to bottom)

```
1. Announcement Bar          - Shipping and delivery message
2. Navigation Header         - Logo, menu, search, and shop button
3. Hero Section             - Large background image with main headline
4. Features Section         - Three feature cards (LED Lighting, Tripods, Pro Equipment)
5. Benefits Section         - Three benefit sections with images
6. Testimonials Section     - Customer reviews and ratings
7. FAQ Section              - Frequently asked questions with accordion
8. Policies Section         - Shipping and Returns information
9. CTA Section              - Call-to-action with background image
10. Footer                  - Links, company info, and copyright
11. Scroll to Top Button    - Fixed button in bottom-right corner
```

### File Organization Recommendation

Create a folder structure like this on your computer:

```
photography-site/
├── index.html              (main landing page)
├── privacy.html            (privacy policy - we'll create this)
├── terms.html              (terms of service - we'll create this)
├── css/
│   └── custom.css          (optional: for custom styles)
└── images/
    └── (store your images here)
```

---

## Updating Text Content

### Finding and Changing Text

Each section of the page contains specific text that you can easily update. Here's how to find and modify the most important ones:

#### 1. **Announcement Bar** (Top of Page)

**Location**: Look for this code near the top (around line 65):

```html
<!-- Announcement Bar -->
<div class="bg-gradient-to-r from-gray-900 to-gray-800 text-white py-3 px-4">
    <div class="max-w-7xl mx-auto flex items-center justify-center text-center">
        <i class="fas fa-truck mr-2"></i>
        <p class="text-sm md:text-base font-medium">Free Worldwide Shipping on Orders Over $50 | Fast 5-Day Delivery</p>
    </div>
</div>
```

**To change the message**:
- Find the text: `Free Worldwide Shipping on Orders Over $50 | Fast 5-Day Delivery`
- Replace it with your message, for example:
  ```html
  <p class="text-sm md:text-base font-medium">New Collection Available! Free Shipping on Orders Over $75</p>
  ```

**Pro Tip**: Keep messages short and impactful. The `text-sm md:text-base` means it's small on mobile and medium-sized on desktop.

---

#### 2. **Logo and Header Text**

**Location**: Around line 80:

```html
<!-- Logo -->
<div class="flex-shrink-0">
    <a href="#" class="text-2xl md:text-3xl font-bold text-gray-900" aria-label="Photography SE Asia Home">
        <i class="fas fa-camera mr-2 text-gray-700"></i>
        <span class="hidden sm:inline">Photography SE Asia</span>
        <span class="sm:hidden">PSA</span>
    </a>
</div>
```

**To change the logo text**:
- **Full name** (shows on tablets/desktops): Replace `Photography SE Asia` with your brand name
- **Short name** (shows on mobile): Replace `PSA` with your 2-3 letter abbreviation

**Example**:
```html
<span class="hidden sm:inline">Your Brand Name</span>
<span class="sm:hidden">YBN</span>
```

---

#### 3. **Hero Section** (Large Banner with Image)

**Location**: Around line 130-150:

```html
<!-- Hero Section -->
<section class="relative w-full h-screen md:h-[600px] overflow-hidden">
    <!-- ... image code ... -->
    <div class="relative z-10 h-full flex items-center justify-center">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center text-white fade-in-up">
            <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-4 md:mb-6 leading-tight tracking-tight">
                Photography SE Asia
            </h1>
            <p class="text-xl md:text-2xl lg:text-3xl font-light mb-8 md:mb-10 leading-relaxed">
                Best Photography Kit In SE Asia
            </p>
            <p class="text-base md:text-lg mb-8 md:mb-12 opacity-90 max-w-2xl mx-auto">
                Discover premium LED lighting, professional tripods, and pro-grade equipment designed for photographers who demand excellence
            </p>
```

**To update the hero text**:

- **Main headline** (biggest text):
  ```html
  <h1>Your New Headline Here</h1>
  ```

- **Subheading** (second line):
  ```html
  <p class="text-xl md:text-2xl lg:text-3xl font-light mb-8 md:mb-10 leading-relaxed">
      Your subheading here
  </p>
  ```

- **Description paragraph**:
  ```html
  <p class="text-base md:text-lg mb-8 md:mb-12 opacity-90 max-w-2xl mx-auto">
      Your description text here
  </p>
  ```

**Example of complete update**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-4 md:mb-6 leading-tight tracking-tight">
    Professional Photo Equipment
</h1>
<p class="text-xl md:text-2xl lg:text-3xl font-light mb-8 md:mb-10 leading-relaxed">
    Premium Gear for Every Photographer
</p>
<p class="text-base md:text-lg mb-8 md:mb-12 opacity-90 max-w-2xl mx-auto">
    Find everything you need to take your photography to the next level
</p>
```

---

#### 4. **Features Section** (Three Cards)

**Location**: Around line 175-250

Each feature card has a title, description, and bullet points. Here's the first card:

```html
<!-- LED Lighting Feature -->
<div class="feature-card bg-gradient-to-br from-gray-50 to-white p-8 md:p-10 rounded-xl border border-gray-200 hover:border-gray-300">
    <div class="bg-gradient-to-br from-yellow-400 to-yellow-500 w-16 h-16 rounded-lg flex items-center justify-center mb-6 shadow-lg">
        <i class="fas fa-lightbulb text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-3">LED Lighting</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Professional-grade LED lighting systems with adjustable color temperature and brightness control for perfect illumination in any environment.
    </p>
    <ul class="space-y-2 text-gray-600">
        <li class="flex items-center">
            <i class="fas fa-check text-yellow-500 mr-3"></i>
            <span>5600K daylight temperature</span>
        </li>
        <li class="flex items-center">
            <i class="fas fa-check text-yellow-500 mr-3"></i>
            <span>Flicker-free technology</span>
        </li>
        <li class="flex items-center">
            <i class="fas fa-check text-yellow-500 mr-3"></i>
            <span>Energy efficient</span>
        </li>
    </ul>
</div>
```

**To update a feature card**:

1. **Change the title**:
   ```html
   <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-3">Your Title Here</h3>
   ```

2. **Change the description**:
   ```html
   <p class="text-gray-600 leading-relaxed mb-4">
       Your description text here
   </p>
   ```

3. **Update bullet points**:
   ```html
   <li class="flex items-center">
       <i class="fas fa-check text-yellow-500 mr-3"></i>
       <span>Your bullet point text</span>
   </li>
   ```

**Complete example - updating the LED Lighting card**:
```html
<h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-3">Studio Lights</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    High-powered LED systems perfect for any studio setup
</p>
<ul class="space-y-2 text-gray-600">
    <li class="flex items-center">
        <i class="fas fa-check text-yellow-500 mr-3"></i>
        <span>Adjustable brightness</span>
    </li>
    <li class="flex items-center">
        <i class="fas fa-check text-yellow-500 mr-3"></i>
        <span>Professional color accuracy</span>
    </li>
    <li class="flex items-center">
        <i class="fas fa-check text-yellow-500 mr-3"></i>
        <span>Long-lasting bulbs</span>
    </li>
</ul>
```

---

#### 5. **Benefits Section** (Free Delivery, Fast Shipping, High Quality)

**Location**: Around line 280-450

Each benefit section has a title, description, bullet points, and a button. Here's the Free Delivery section:

```html
<!-- Benefit 1: Free Delivery (Text Left) -->
<div class="mb-16 md:mb-24">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 md:gap-12 items-center bg-white rounded-2xl overflow-hidden shadow-lg">
        <div class="p-8 md:p-12">
            <div class="flex items-center mb-6">
                <div class="w-16 h-16 bg-gradient-to-br from-green-400 to-green-500 rounded-lg flex items-center justify-center shadow-lg">
                    <i class="fas fa-shipping-fast text-white text-2xl"></i>
                </div>
                <h3 class="text-3xl md:text-4xl font-bold text-gray-900 ml-4">Free Delivery</h3>
            </div>
            <p class="text-gray-600 text-lg leading-relaxed mb-6">
                Enjoy complimentary shipping on all orders across Southeast Asia...
            </p>
            <ul class="space-y-3 mb-8">
                <li class="flex items-center text-gray-700">
                    <i class="fas fa-check-circle text-green-500 mr-3 text-xl"></i>
                    <span>No minimum purchase required</span>
                </li>
                <!-- more items -->
            </ul>
        </div>
    </div>
</div>
```

**To update benefits**:

1. **Change the title**:
   ```html
   <h3 class="text-3xl md:text-4xl font-bold text-gray-900 ml-4">Your Title</h3>
   ```

2. **Change the main description**:
   ```html
   <p class="text-gray-600 text-lg leading-relaxed mb-6">
       Your description here
   </p>
   ```

3. **Update bullet points**:
   ```html
   <li class="flex items-center text-gray-700">
       <i class="fas fa-check-circle text-green-500 mr-3 text-xl"></i>
       <span>Your benefit point</span>
   </li>
   ```

---

#### 6. **Testimonials Section** (Customer Reviews)

**Location**: Around line 480-560

Each testimonial card contains a review:

```html
<!-- Testimonial 1 -->
<div class="testimonial-card bg-gradient-to-br from-gray-50 to-white p-8 md:p-10 rounded-xl border border-gray-200">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
        <span class="text-gray-600 ml-2 font-semibold">5.0</span>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "The LED lighting kit I purchased has completely transformed my studio setup. The quality is exceptional and the free delivery made it even better. Highly recommended!"
    </p>
    <div class="flex items-center">
        <div class="w-12 h-12 bg-gradient-to-br from-blue-400 to-blue-500 rounded-full flex items-center justify-center text-white font-bold mr-4">
            MC
        </div>
        <div>
            <p class="font-bold text-gray-900">Marcus Chen</p>
            <p class="text-gray-600 text-sm">Professional Photographer, Bangkok</p>
        </div>
    </div>
</div>
```

**To update a testimonial**:

1. **Change the review text**:
   ```html
   <p class="text-gray-700 leading-relaxed mb-6">
       "Your new review text here"
   </p>
   ```

2. **Change the customer name**:
   ```html
   <p class="font-bold text-gray-900">New Customer Name</p>
   ```

3. **Change the customer title/location**:
   ```html
   <p class="text-gray-600 text-sm">Your Title, Your Location</p>
   ```

4. **Change the initials** (the colored circle):
   ```html
   <div class="w-12 h-12 bg-gradient-to-br from-blue-400 to-blue-500 rounded-full flex items-center justify-center text-white font-bold mr-4">
       NC
   </div>
   ```

---

#### 7. **FAQ Section** (Frequently Asked Questions)

**Location**: Around line 590-700

Each FAQ item has a question and answer:

```html
<!-- FAQ Item 1 -->
<div class="accordion-item bg-white rounded-lg border border-gray-200 overflow-hidden">
    <button class="w-full px-6 md:px-8 py-4 md:py-6 flex items-center justify-between hover:bg-gray-50 transition focus:outline-none focus:ring-2 focus:ring-gray-900 focus:ring-offset-2" onclick="toggleAccordion(this)">
        <span class="text-lg md:text-xl font-bold text-gray-900 text-left">What is included in the pro equipment package?</span>
        <i class="fas fa-chevron-down text-gray-600 transition"></i>
    </button>
    <div class="accordion-content px-6 md:px-8 py-4 md:py-6 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            Our pro equipment package includes professional-grade LED lighting systems...
        </p>
    </div>
</div>
```

**To update FAQ items**:

1. **Change the question**:
   ```html
   <span class="text-lg md:text-xl font-bold text-gray-900 text-left">Your new question here?</span>
   ```

2. **Change the answer**:
   ```html
   <p class="text-gray-700 leading-relaxed">
       Your answer text here
   </p>
   ```

---

#### 8. **Footer** (Bottom of Page)

**Location**: Around line 800-900

The footer has company info, quick links, support links, and legal links:

```html
<!-- Company Info -->
<div>
    <h3 class="text-white font-bold text-lg mb-4">Photography SE Asia</h3>
    <p class="text-gray-400 text-sm leading-relaxed mb-4">
        Premium photography equipment and lighting solutions for professionals across Southeast Asia.
    </p>
</div>
```

**To update footer company info**:
```html
<h3 class="text-white font-bold text-lg mb-4">Your Company Name</h3>
<p class="text-gray-400 text-sm leading-relaxed mb-4">
    Your company description here
</p>
```

**Footer copyright** (very bottom):
```html
<p class="text-gray-400 text-sm">
    &copy; 2024 Photography SE Asia. All rights reserved.
</p>
```

To update the year and company name:
```html
<p class="text-gray-400 text-sm">
    &copy; 2025 Your Company Name. All rights reserved.
</p>
```

---

### Text Update Checklist

Use this checklist to ensure you've updated all key text:

- [ ] Announcement bar message
- [ ] Logo text (full and short versions)
- [ ] Hero section headline
- [ ] Hero section subheading
- [ ] Hero section description
- [ ] Feature 1 title and description
- [ ] Feature 1 bullet points
- [ ] Feature 2 title and description
- [ ] Feature 2 bullet points
- [ ] Feature 3 title and description
- [ ] Feature 3 bullet points
- [ ] Benefit titles and descriptions
- [ ] Benefit bullet points
- [ ] Testimonials (reviews, names, locations)
- [ ] FAQ questions and answers
- [ ] Footer company name and description
- [ ] Footer copyright year

---

## Working with Tailwind CSS Classes

### What are Tailwind CSS Classes?

Tailwind CSS is a system for styling web pages using special class names. Instead of writing complex CSS code, you add these class names directly to HTML elements. This page uses Tailwind extensively.

**Example**:
```html
<!-- This creates a button with styling -->
<button class="bg-white text-gray-900 px-8 py-4 rounded-lg font-bold">
    Click Me
</button>
```

Let's break down what each class does:
- `bg-white` = white background
- `text-gray-900` = dark gray text
- `px-8` = padding (space inside) on left and right
- `py-4` = padding (space inside) on top and bottom
- `rounded-lg` = slightly rounded corners
- `font-bold` = make text bold

### Common Tailwind Classes Used in This Page

#### **Colors**

The page uses a color system. Here are the main ones:

| Class | What It Does | Example |
|-------|-------------|---------|
| `bg-white` | White background | `<div class="bg-white">` |
| `bg-gray-50` | Very light gray background | `<div class="bg-gray-50">` |
| `bg-gray-900` | Very dark gray/black background | `<div class="bg-gray-900">` |
| `text-white` | White text | `<p class="text-white">` |
| `text-gray-600` | Medium gray text | `<p class="text-gray-600">` |
| `text-gray-900` | Dark gray text | `<p class="text-gray-900">` |
| `bg-yellow-400` | Bright yellow | `<div class="bg-yellow-400">` |
| `bg-blue-500` | Bright blue | `<div class="bg-blue-500">` |
| `bg-green-500` | Bright green | `<div class="bg-green-500">` |

#### **Text Size**

| Class | Size | Where Used |
|-------|------|-----------|
| `text-sm` | Small (12px) | Announcement bar, small text |
| `text-base` | Normal (16px) | Body text |
| `text-lg` | Large (18px) | Descriptions |
| `text-xl` | Extra large (20px) | Subheadings |
| `text-2xl` | 24px | Section headings |
| `text-3xl` | 30px | Large headings |
| `text-4xl` | 36px | Very large headings |
| `text-5xl` | 48px | Hero section headings |

#### **Text Style**

| Class | What It Does |
|-------|-------------|
| `font-bold` | Make text bold |
| `font-semibold` | Make text semi-bold |
| `font-light` | Make text light/thin |
| `text-center` | Center text |
| `text-left` | Align text left |
| `leading-relaxed` | Increase space between lines |
| `tracking-tight` | Decrease space between letters |

#### **Spacing (Padding & Margin)**

Padding is space **inside** an element. Margin is space **outside**.

| Class | Meaning |
|-------|---------|
| `p-4` | Padding of 16px on all sides |
| `p-8` | Padding of 32px on all sides |
| `px-4` | Padding of 16px left and right |
| `py-4` | Padding of 16px top and bottom |
| `m-4` | Margin of 16px on all sides |
| `mb-6` | Margin of 24px on bottom |
| `mr-2` | Margin of 8px on right |

#### **Sizing**

| Class | Meaning |
|-------|---------|
| `w-12` | Width of 48px |
| `h-12` | Height of 48px |
| `w-full` | Width of 100% (full width) |
| `h-full` | Height of 100% (full height) |

#### **Border and Rounded Corners**

| Class | What It Does |
|-------|-------------|
| `border` | Add a border |
| `border-gray-200` | Light gray border |
| `rounded-lg` | Slightly rounded corners |
| `rounded-xl` | Very rounded corners |
| `rounded-full` | Circle |

#### **Responsive Design Classes**

These classes make the page look good on all screen sizes:

| Class | Meaning |
|-------|---------|
| `md:` | Apply this style on medium screens and larger (tablets) |
| `lg:` | Apply this style on large screens (desktops) |
| `sm:` | Apply this style on small screens and larger |
| `hidden` | Hide this element |
| `md:hidden` | Hide on medium screens and larger |
| `hidden md:flex` | Hide by default, show on medium screens |

**Example**:
```html
<h1 class="text-2xl md:text-4xl lg:text-5xl">
    Responsive Heading
</h1>
```

This means:
- On mobile: text size 2xl (24px)
- On tablets (md): text size 4xl (36px)
- On desktops (lg): text size 5xl (48px)

---

### Modifying Tailwind Classes

#### **Changing Button Colors**

Find the button you want to change:

```html
<a href="https://ledx.com" class="btn-primary bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-gray-800 transition">
    Shop Now
</a>
```

To change the button color:

**Original (dark gray/black)**:
```html
class="btn-primary bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-gray-800 transition"
```

**Change to blue**:
```html
class="btn-primary bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition"
```

**Change to green**:
```html
class="btn-primary bg-green-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-green-700 transition"
```

**Explanation**:
- `bg-gray-900` = background color (change this)
- `text-white` = text color (keep white for contrast)
- `hover:bg-gray-800` = color when you hover over it (make it slightly darker)

---

#### **Changing Text Colors**

Find text you want to change:

```html
<p class="text-gray-600 leading-relaxed">
    Your text here
</p>
```

**Change to darker gray**:
```html
<p class="text-gray-900 leading-relaxed">
```

**Change to lighter gray**:
```html
<p class="text-gray-500 leading-relaxed">
```

---

#### **Changing Background Colors**

Find a section with a background:

```html
<section class="py-16 md:py-24 bg-white">
```

**Change to light gray**:
```html
<section class="py-16 md:py-24 bg-gray-50">
```

**Change to dark gray**:
```html
<section class="py-16 md:py-24 bg-gray-900">
```

---

#### **Changing Spacing**

Find an element with padding or margin:

```html
<div class="p-8 md:p-12">
    Content here
</div>
```

This means: padding of 32px on mobile, 48px on tablets/desktops.

**To make it more spacious**:
```html
<div class="p-12 md:p-16">
```

**To make it more compact**:
```html
<div class="p-4 md:p-8">
```

---

#### **Changing Text Size**

Find text you want to resize:

```html
<h3 class="text-2xl md:text-3xl font-bold">
    Feature Title
</h3>
```

This means: 24px on mobile, 30px on tablets/desktops.

**Make it larger**:
```html
<h3 class="text-3xl md:text-4xl font-bold">
```

**Make it smaller**:
```html
<h3 class="text-xl md:text-2xl font-bold">
```

---

### Common Tailwind Modifications for This Page

#### **Modifying Feature Cards**

Location: Around line 200

Current styling:
```html
<div class="feature-card bg-gradient-to-br from-gray-50 to-white p-8 md:p-10 rounded-xl border border-gray-200 hover:border-gray-300">
```

**To make cards more colorful**:
```html
<div class="feature-card bg-gradient-to-br from-blue-50 to-blue-100 p-8 md:p-10 rounded-xl border border-blue-300 hover:border-blue-400">
```

**To add more shadow** (make it "pop"):
```html
<div class="feature-card bg-gradient-to-br from-gray-50 to-white p-8 md:p-10 rounded-xl border border-gray-200 hover:border-gray-300 shadow-lg hover:shadow-xl">
```

---

#### **Modifying Section Spacing**

Find a section tag:
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

This means: 64px padding top/bottom on mobile, 96px on tablets/desktops.

**To add more space**:
```html
<section id="features" class="py-20 md:py-32 bg-white">
```

**To reduce space**:
```html
<section id="features" class="py-12 md:py-16 bg-white">
```

---

#### **Making Text Larger or Smaller**

Find heading:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold">
    Premium Photography Equipment
</h2>
```

**Make all sizes larger**:
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold">
```

**Make all sizes smaller**:
```html
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold">
```

---

### Tailwind Reference for This Page

**Quick reference for common values**:

- **Spacing values**: 2, 4, 6, 8, 10, 12, 16, 20, 24, 32, 40, 48, 56, 64
- **Text sizes**: sm, base, lg, xl, 2xl, 3xl, 4xl, 5xl, 6xl
- **Colors**: 50, 100, 200, 300, 400, 500, 600, 700, 800, 900 (higher = darker)
- **Responsive breakpoints**: `sm:` (640px), `md:` (768px), `lg:` (1024px)

---

## Fixing and Managing Links

### Understanding Links on This Page

Links are what make websites interactive. They take users to other pages or websites. This page has many links that you may need to update.

### Types of Links on This Page

1. **External Links** - Go to other websites (like your shop)
2. **Internal Links** - Go to other pages within your site (like privacy.html)
3. **Anchor Links** - Jump to sections on the same page (like #features)

---

### All Links on This Page (Complete List)

Here's every link on the page that you might need to update:

#### **Navigation Links**

**Location**: Around line 85-95 (desktop menu)

```html
<nav class="hidden md:flex items-center space-x-8">
    <a href="#features" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Features</a>
    <a href="#benefits" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Benefits</a>
    <a href="#faq" class="nav-link text-gray-700 hover:text-gray-900 font-medium">FAQ</a>
    <a href="#testimonials" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Reviews</a>
</nav>
```

**Status**: ✅ These links work correctly (they jump to sections on the page)

---

#### **Search and Shop Buttons**

**Location**: Around line 100-110

```html
<div class="hidden lg:flex items-center space-x-4">
    <input type="text" placeholder="Search products..." class="bg-gray-100 text-gray-900 px-4 py-2 rounded-lg focus:outline-none focus:ring-2 focus:ring-gray-700 transition" aria-label="Search products">
    <a href="https://ledx.com" class="btn-primary bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-gray-800 transition">
        Shop Now
    </a>
</div>
```

**Status**: ⚠️ The "Shop Now" button links to `https://ledx.com` - **You need to change this to your actual shop URL**

---

#### **Mobile Shop Button**

**Location**: Around line 115-120

```html
<a href="https://ledx.com" class="bg-gray-900 text-white px-4 py-2 rounded-lg font-semibold hover:bg-gray-800 transition text-sm">
    Shop
</a>
```

**Status**: ⚠️ Same as above - **Change to your shop URL**

---

#### **Mobile Navigation Links**

**Location**: Around line 130-140

```html
<nav id="mobile-menu" class="hidden md:hidden pb-4 space-y-2">
    <a href="#features" class="block text-gray-700 hover:text-gray-900 font-medium py-2 px-4 rounded hover:bg-gray-100 transition">Features</a>
    <a href="#benefits" class="block text-gray-700 hover:text-gray-900 font-medium py-2 px-4 rounded hover:bg-gray-100 transition">Benefits</a>
    <a href="#faq" class="block text-gray-700 hover:text-gray-900 font-medium py-2 px-4 rounded hover:bg-gray-100 transition">FAQ</a>
    <a href="#testimonials" class="block text-gray-700 hover:text-gray-900 font-medium py-2 px-4 rounded hover:bg-gray-100 transition">Reviews</a>
</nav>
```

**Status**: ✅ These links work correctly

---

#### **Hero Section Buttons**

**Location**: Around line 185-195

```html
<div class="flex flex-col sm:flex-row gap-4 justify-center">
    <a href="https://ledx.com" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition inline-block">
        Explore Collection
    </a>
    <a href="#features" class="btn-primary bg-transparent border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-gray-900 transition inline-block">
        Learn More
    </a>
</div>
```

**Status**: 
- ⚠️ "Explore Collection" links to `https://ledx.com` - **Change this**
- ✅ "Learn More" links to #features - **This is correct**

---

#### **Benefits Section Buttons**

**Location**: Around line 360, 410, 460

There are three benefit buttons:

```html
<!-- Free Delivery button -->
<a href="https://ledx.com" class="btn-primary inline-block bg-green-500 text-white px-8 py-3 rounded-lg font-bold hover:bg-green-600 transition">
    Shop Now
</a>

<!-- Fast Shipping button -->
<a href="https://ledx.com" class="btn-primary inline-block bg-blue-500 text-white px-8 py-3 rounded-lg font-bold hover:bg-blue-600 transition">
    Order Today
</a>

<!-- High Quality button -->
<a href="https://ledx.com" class="btn-primary inline-block bg-red-500 text-white px-8 py-3 rounded-lg font-bold hover:bg-red-600 transition">
    Browse Products
</a>
```

**Status**: ⚠️ All three link to `https://ledx.com` - **Change these**

---

#### **CTA Section Buttons**

**Location**: Around line 750-760

```html
<div class="flex flex-col sm:flex-row gap-4 justify-center">
    <a href="https://ledx.com" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition inline-block">
        Shop Premium Kits
    </a>
    <a href="mailto:adminx@led.com" class="btn-primary bg-transparent border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-gray-900 transition inline-block">
        Contact Us
    </a>
</div>
```

**Status**: 
- ⚠️ "Shop Premium Kits" links to `https://ledx.com` - **Change this**
- ⚠️ "Contact Us" links to `mailto:adminx@led.com` - **Change this to your email**

---

#### **Footer Links**

**Location**: Around line 800-900

The footer has many sections with links:

**Quick Links Section**:
```html
<li>
    <a href="https://ledx.com" class="text-gray-400 hover:text-white transition text-sm">
        Shop Products
    </a>
</li>
```

**Support Section**:
```html
<li>
    <a href="mailto:adminx@led.com" class="text-gray-400 hover:text-white transition text-sm">
        Contact Us
    </a>
</li>
```

**Legal Section** (THIS IS IMPORTANT):
```html
<li>
    <a href="#" class="text-gray-400 hover:text-white transition text-sm">
        Privacy Policy
    </a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white transition text-sm">
        Terms of Service
    </a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white transition text-sm">
        Cookie Policy
    </a>
</li>
<li>
    <a href="#" class="text-gray-400 hover:text-white transition text-sm">
        Disclaimer
    </a>
</li>
```

**Status**: 
- ⚠️ Shop link needs to be updated to your shop URL
- ⚠️ Contact Us email needs to be updated to your email
- ❌ Privacy Policy, Terms of Service, Cookie Policy, and Disclaimer all link to `#` - **These need to be fixed**

**Footer Bottom**:
```html
<p class="text-gray-400 text-sm flex items-center">
    <i class="fas fa-envelope mr-2"></i>
    <a href="mailto:adminx@led.com" class="hover:text-white transition">
        adminx@led.com
    </a>
</p>
<p class="text-gray-400 text-sm flex items-center">
    <i class="fas fa-globe mr-2"></i>
    <a href="https://ledx.com" class="hover:text-white transition">
        Visit Store
    </a>
</p>
```

**Status**: ⚠️ Both need to be updated to your information

---

### Step-by-Step: How to Update Links

#### **Step 1: Identify the Link**

Find the `<a>` tag (link) you want to change. Look for the `href=` part:

```html
<a href="https://ledx.com">Shop Now</a>
```

The part in quotes after `href=` is the link address.

#### **Step 2: Determine Your New Link**

Before you change it, know what the new link should be:

- **Your shop URL**: `https://yourshopname.com` (get this from your shop provider)
- **Your email**: `your-email@example.com`
- **Your privacy page**: `privacy.html` (if it's on your server)
- **Your terms page**: `terms.html` (if it's on your server)

#### **Step 3: Replace the Old Link**

**Example 1: Change the Shop URL**

**Before**:
```html
<a href="https://ledx.com" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition inline-block">
    Explore Collection
</a>
```

**After**:
```html
<a href="https://myshop.com/products" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition inline-block">
    Explore Collection
</a>
```

**Example 2: Change the Email**

**Before**:
```html
<a href="mailto:adminx@led.com" class="btn-primary bg-transparent border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-gray-900 transition inline-block">
    Contact Us
</a>
```

**After**:
```html
<a href="mailto:contact@yourcompany.com" class="btn-primary bg-transparent border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-gray-900 transition inline-block">
    Contact Us
</a>
```

#### **Step 4: Save and Test**

1. Save your file (Ctrl+S or Cmd+S)
2. Refresh your browser (F5)
3. Click the link to make sure it works

---

### Complete Link Update Checklist

Use this checklist to update all links:

#### **External Links (to your shop)**
Find every instance of `https://ledx.com` and replace with your shop URL:

```
Search for: https://ledx.com
Replace with: https://yourshop.com
```

**Locations**:
- [ ] Line ~103 - Shop Now button (desktop)
- [ ] Line ~117 - Shop button (mobile)
- [ ] Line ~189 - Explore Collection button (hero)
- [ ] Line ~363 - Shop Now button (Free Delivery)
- [ ] Line ~413 - Order Today button (Fast Shipping)
- [ ] Line ~463 - Browse Products button (High Quality)
- [ ] Line ~753 - Shop Premium Kits button (CTA)
- [ ] Line ~849 - Shop Products link (footer)
- [ ] Line ~923 - Visit Store link (footer)

#### **Email Links**
Find every instance of `mailto:adminx@led.com` and replace with your email:

```
Search for: mailto:adminx@led.com
Replace with: mailto:your-email@yourcompany.com
```

**Locations**:
- [ ] Line ~756 - Contact Us button (CTA)
- [ ] Line ~866 - Contact Us link (footer)
- [ ] Line ~918 - Email address link (footer)

#### **Policy Pages** (we'll create these next)
Find every instance of `#` in the Legal section and replace:

```
Search for: href="#" (in Legal section)
Replace with: href="privacy.html" or href="terms.html"
```

**Locations**:
- [ ] Line ~877 - Privacy Policy
- [ ] Line ~882 - Terms of Service
- [ ] Line ~887 - Cookie Policy
- [ ] Line ~892 - Disclaimer

---

### Quick Link Update Guide

**Most Important Links to Update**:

1. **Shop URL** (appears 8 times)
   - Find: `https://ledx.com`
   - Replace with: Your shop URL

2. **Email Address** (appears 3 times)
   - Find: `adminx@led.com`
   - Replace with: Your email address

3. **Policy Pages** (appears 4 times)
   - Find: `href="#"` (in Legal section only)
   - Replace with: `href="privacy.html"`, `href="terms.html"`, etc.

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

Privacy and Terms pages are legally required for most websites. They explain:
- **Privacy Policy**: How you collect and use customer data
- **Terms of Service**: The rules for using your website

### Creating Your Privacy Policy Page

#### **Step 1: Create a New File**

1. Open your text editor (same one you use for index.html)
2. Click **File** → **New**
3. Copy and paste the code below
4. Click **File** → **Save As**
5. Name it: `privacy.html`
6. Save it in the same folder as `index.html`

#### **Step 2: Privacy Policy Template**

Here's a complete privacy policy page that matches your site's design:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Photography SE Asia">
    <title>Privacy Policy - Photography SE Asia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Playfair Display', serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16 md:h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl md:text-3xl font-bold text-gray-900" aria-label="Photography SE Asia Home">
                        <i class="fas fa-camera mr-2 text-gray-700"></i>
                        <span class="hidden sm:inline">Photography SE Asia</span>
                        <span class="sm:hidden">PSA</span>
                    </a>
                </div>
                <a href="index.html" class="text-gray-700 hover:text-gray-900 font-medium">
                    Back to Home
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Privacy Policy</h1>
        <p class="text-gray-600 mb-8">Last updated: January 2024</p>

        <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>Photography SE Asia ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, shipping address, and payment information when you make a purchase</li>
                    <li><strong>Device Information:</strong> Browser type, IP address, operating system, and referring URLs</li>
                    <li><strong>Usage Data:</strong> Pages visited, time spent on pages, and links clicked</li>
                    <li><strong>Cookies:</strong> We use cookies to enhance your browsing experience</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. How We Use Your Information</h2>
                <p>Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Process your transactions and send related information</li>
                    <li>Email you regarding your order status or other account information</li>
                    <li>Fulfill and manage purchases, orders, payments, and other transactions related to the Site</li>
                    <li>Generate a personal profile about you so that future visits to the Site will be personalized</li>
                    <li>Increase the efficiency and operation of the Site</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p>We may share information we have collected about you in certain situations:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li><strong>By Law or to Protect Rights:</strong> If required by law or to protect our rights</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with vendors, consultants, and other service providers who need access to such information to carry out work on our behalf</li>
                    <li><strong>Business Transfers:</strong> If we are involved in a merger, acquisition, or sale of assets</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p>We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or method of electronic storage is 100% secure.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>If you have questions or comments about this Privacy Policy, please contact us at:</p>
                <p class="mt-4">
                    <strong>Photography SE Asia</strong><br>
                    Email: <a href="mailto:contact@photographyseasia.com" class="text-blue-600 hover:text-blue-800">contact@photographyseasia.com</a><br>
                    Website: <a href="index.html" class="text-blue-600 hover:text-blue-800">https://yourwebsite.com</a>
                </p>
            </section>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <p class="text-center text-gray-400">
                &copy; 2024 Photography SE Asia. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Creating Your Terms of Service Page

#### **Step 1: Create a New File**

1. Open your text editor
2. Click **File** → **New**
3. Copy and paste the code below
4. Click **File** → **Save As**
5. Name it: `terms.html`
6. Save it in the same folder as `index.html`

#### **Step 2: Terms of Service Template**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Photography SE Asia">
    <title>Terms of Service - Photography SE Asia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Playfair Display', serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16 md:h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl md:text-3xl font-bold text-gray-900" aria-label="Photography SE Asia Home">
                        <i class="fas fa-camera mr-2 text-gray-700"></i>
                        <span class="hidden sm:inline">Photography SE Asia</span>
                        <span class="sm:hidden">PSA</span>
                    </a>
                </div>
                <a href="index.html" class="text-gray-700 hover:text-gray-900 font-medium">
                    Back to Home
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Terms of Service</h1>
        <p class="text-gray-600 mb-8">Last updated: January 2024</p>

        <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>Permission is granted to temporarily download one copy of the materials (information or software) on Photography SE Asia's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>The materials on Photography SE Asia's website are provided on an 'as is' basis. Photography SE Asia makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>In no event shall Photography SE Asia or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Photography SE Asia's website.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>The materials appearing on Photography SE Asia's website could include technical, typographical, or photographic errors. Photography SE Asia does not warrant that any of the materials on the website are accurate, complete, or current. Photography SE Asia may make changes to the materials contained on its website at any time without notice.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>Photography SE Asia has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Photography SE Asia of the site. Use of any such linked website is at the user's own risk.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>Photography SE Asia may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>These terms and conditions are governed by and construed in accordance with the laws of Southeast Asia, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Information</h2>
                <p>If you have any questions about these Terms of Service, please contact us at:</p>
                <p class="mt-4">
                    <strong>Photography SE Asia</strong><br>
                    Email: <a href="mailto:contact@photographyseasia.com" class="text-blue-600 hover:text-blue-800">contact@photographyseasia.com</a><br>
                    Website: <a href="index.html" class="text-blue-600 hover:text-blue-800">https://yourwebsite.com</a>
                </p>
            </section>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <p class="text-center text-gray-400">
                &copy; 2024 Photography SE Asia. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Linking the Policy Pages to Your Main Page

Now that you've created the policy pages, you need to link them from your main `index.html` file.

#### **Step 1: Find the Footer Legal Section**

In your `index.html`, find the Legal section in the footer (around line 875-895):

```html
<!-- Legal -->
<div>
    <h3 class="text-white font-bold text-lg mb-4">Legal</h3>
    <ul class="space-y-2">
        <li>
            <a href="#" class="text-gray-400 hover:text-white transition text-sm">
                Privacy Policy
            </a>
        </li>
        <li>
            <a href="#" class="text-gray-400 hover:text-white transition text-sm">
                Terms of Service
            </a>
        </li>
        <li>
            <a href="#" class="text-gray-400 hover:text-white transition text-sm">
                Cookie Policy
            </a>
        </li>
        <li>
            <a href="#" class="text-gray-400 hover:text-white transition text-sm">
                Disclaimer
            </a>
        </li>
    </ul>
</div>
```

#### **Step 2: Replace the Links**

Change each `href="#"` to point to your new pages:

```html
<!-- Legal -->
<div>
    <h3 class="text-white font-bold text-lg mb-4">Legal</h3>
    <ul class="space-y-2">
        <li>
            <a href="privacy.html" class="text-gray-400 hover:text-white transition text-sm">
                Privacy Policy
            </a>
        </li>
        <li>
            <a href="terms.html" class="text-gray-400 hover:text-white transition text-sm">
                Terms of Service
            </a>
        </li>
        <li>
            <a href="privacy.html" class="text-gray-400 hover:text-white transition text-sm">
                Cookie Policy
            </a>
        </li>
        <li>
            <a href="terms.html" class="text-gray-400 hover:text-white transition text-sm">
                Disclaimer
            </a>
        </li>
    </ul>
</div>
```

**Explanation**:
- `href="privacy.html"` = Link to the privacy policy page
- `href="terms.html"` = Link to the terms of service page
- You can link Cookie Policy and Disclaimer to either page, or create separate pages if you prefer

#### **Step 3: Save and Test**

1. Save your `index.html` file
2. Refresh your browser
3. Scroll to the footer and click on "Privacy Policy" - it should open your new privacy.html page
4. Click "Back to Home" to return to the main page
5. Test the other policy links

---

### Customizing Your Policy Pages

The templates I provided are generic. You should customize them with your specific information:

#### **In privacy.html**, change:
- Email address: Replace `contact@photographyseasia.com` with your email
- Website URL: Replace `https://yourwebsite.com` with your actual website
- Add any specific information about your data collection practices

#### **In terms.html**, change:
- Email