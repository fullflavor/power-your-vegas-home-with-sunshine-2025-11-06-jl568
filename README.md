# SolarVegas Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain, update, and customize your SolarVegas landing page. Whether you're updating text, fixing links, or adding new content, you'll find step-by-step instructions tailored specifically to your page structure.

---

## Table of Contents

1. [Understanding Your Page Structure](#understanding-your-page-structure)
2. [Updating Text and Content](#updating-text-and-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Updating Links](#fixing-and-updating-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Troubleshooting Guide](#troubleshooting-guide)
7. [Best Practices](#best-practices)

---

## Understanding Your Page Structure

Before making changes, it's helpful to understand how your landing page is organized. Your `index.html` file contains several major sections:

### Page Sections Overview

| Section | Purpose | Location in File |
|---------|---------|------------------|
| **Header & Navigation** | Top menu bar with logo and links | Lines 44-97 |
| **Hero Section** | Main banner with headline and CTA buttons | Lines 99-178 |
| **Features Section** | Three feature cards (Energy Audit, System Design, Solar Panels) | Lines 180-261 |
| **Benefits Section** | Three benefit cards plus additional benefits grid | Lines 263-376 |
| **Testimonials Section** | Four customer testimonial cards | Lines 378-445 |
| **About Us Section** | Company information with image | Lines 447-491 |
| **FAQ Section** | Expandable FAQ accordion | Lines 493-615 |
| **CTA Section** | Final call-to-action banner | Lines 617-639 |
| **Footer** | Company info, links, and contact details | Lines 641-719 |
| **JavaScript** | Interactive functionality (mobile menu, FAQ accordion) | Lines 721-800 |

### Key Concepts to Know

**HTML Tags**: These are the building blocks of your page. They look like `<div>`, `<section>`, `<h1>`, etc. Content goes between the opening tag (`<tag>`) and closing tag (`</tag>`).

**Classes**: These are styling instructions written in the `class=""` attribute. Your page uses **Tailwind CSS**, which provides pre-made styling classes like `text-white`, `bg-purple-600`, etc.

**Responsive Design**: Your page automatically adjusts for different screen sizes (phones, tablets, desktops) using classes like `md:` and `lg:` prefixes.

---

## Updating Text and Content

### Section 1: Header & Navigation

The header appears at the top of every page and contains your logo and menu links.

#### **Updating the Logo Text**

**Location**: Lines 50-56

**Current Code**:
```html
<div class="flex items-center space-x-2">
    <div class="gradient-accent w-10 h-10 rounded-lg flex items-center justify-center">
        <i class="fas fa-sun text-white text-lg"></i>
    </div>
    <span class="text-xl font-bold text-gray-900">SolarVegas</span>
</div>
```

**To Change the Logo Text**:
1. Find the line with `<span class="text-xl font-bold text-gray-900">SolarVegas</span>`
2. Replace `SolarVegas` with your company name
3. Example: `<span class="text-xl font-bold text-gray-900">My Solar Company</span>`

**To Change the Logo Icon**:
1. The sun icon uses Font Awesome (a free icon library)
2. Find: `<i class="fas fa-sun text-white text-lg"></i>`
3. Visit [fontawesome.com](https://fontawesome.com/icons) to find another icon
4. Replace `fa-sun` with your chosen icon (e.g., `fa-lightbulb`, `fa-bolt`)
5. Example: `<i class="fas fa-bolt text-white text-lg"></i>`

#### **Updating Navigation Menu Items**

**Location**: Lines 59-64 (Desktop Menu) and Lines 75-82 (Mobile Menu)

**Desktop Menu Code**:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
    <a href="#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Testimonials</a>
    <a href="#faq" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">FAQ</a>
    <a href="https://americashomecontractors.com/actnow" class="btn-primary text-white px-6 py-2 rounded-lg font-semibold">Get Started</a>
</div>
```

**To Change Menu Text**:
1. Find the menu link you want to change
2. Replace the text between `>` and `</a>`
3. Example: Change `<a href="#features">Features</a>` to `<a href="#features">Our Services</a>`

**Important**: The mobile menu (lines 75-82) has the same links and should be updated identically to keep both menus consistent.

---

### Section 2: Hero Section (Main Banner)

The hero section is the large banner at the top with the main headline and call-to-action buttons.

#### **Updating the Main Headline**

**Location**: Line 124

**Current Code**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight">
    Power Your Vegas Home with Sunshine!
</h1>
```

**To Update**:
1. Find the `<h1>` tag in the hero section
2. Replace the text between `>` and `</h1>`
3. Example: `<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight">Get Premium Solar Energy Today</h1>`

**Understanding the Classes**:
- `text-4xl md:text-5xl lg:text-6xl`: Text size changes on different screens (4xl on phones, 5xl on tablets, 6xl on desktops)
- `font-bold`: Makes text bold
- `text-gray-900`: Dark gray text color
- `leading-tight`: Reduces space between lines

#### **Updating the Subheadline**

**Location**: Line 128

**Current Code**:
```html
<p class="text-lg md:text-xl text-gray-600 leading-relaxed max-w-lg">
    Embrace clean energy and slash your electricity bills with our premium solar solutions. Transform your home into a sustainable energy powerhouse and start saving from day one.
</p>
```

**To Update**:
1. Replace the text between `>` and `</p>`
2. Keep the class names the same
3. Example:
```html
<p class="text-lg md:text-xl text-gray-600 leading-relaxed max-w-lg">
    Save up to 90% on your energy bills with our expert solar installation services.
</p>
```

#### **Updating the Main CTA Button Text**

**Location**: Line 133

**Current Code**:
```html
<a href="https://americashomecontractors.com/actnow" class="btn-primary text-white px-8 py-4 rounded-lg font-bold text-lg inline-flex items-center justify-center space-x-2 hover:shadow-xl">
    <span>Get Your Free Energy Audit</span>
    <i class="fas fa-arrow-right"></i>
</a>
```

**To Update Button Text**:
1. Find the `<span>` with the button text
2. Replace the text: `<span>Get Your Free Energy Audit</span>`
3. Example: `<span>Schedule Your Free Consultation</span>`

**To Update Button Link**:
1. Find the `href="https://americashomecontractors.com/actnow"`
2. Replace with your URL: `href="https://yourwebsite.com/contact"`
3. See the "Fixing and Updating Links" section below for more details

#### **Updating the Hero Statistics**

**Location**: Lines 142-155

**Current Code**:
```html
<div class="grid grid-cols-3 gap-4 pt-8">
    <div class="text-center">
        <div class="text-3xl font-bold text-purple-600">98%</div>
        <p class="text-sm text-gray-600">Customer Satisfaction</p>
    </div>
    <div class="text-center">
        <div class="text-3xl font-bold text-purple-600">2500+</div>
        <p class="text-sm text-gray-600">Homes Powered</p>
    </div>
    <div class="text-center">
        <div class="text-3xl font-bold text-purple-600">$50M+</div>
        <p class="text-sm text-gray-600">Saved by Customers</p>
    </div>
</div>
```

**To Update Statistics**:
1. Replace the numbers (e.g., `98%`, `2500+`, `$50M+`)
2. Replace the labels (e.g., `Customer Satisfaction`)
3. Example:
```html
<div class="text-3xl font-bold text-purple-600">95%</div>
<p class="text-sm text-gray-600">Customers Recommend Us</p>
```

---

### Section 3: Features Section

Three feature cards describing your main services.

#### **Updating Feature Card Titles and Descriptions**

**Location**: Lines 180-261

**First Feature Card (Free Home Energy Audit)**:
```html
<div class="feature-card bg-gradient-to-br from-gray-50 to-white rounded-2xl p-8 border border-gray-200 hover:border-purple-300 hover:shadow-xl">
    <div class="w-16 h-16 gradient-accent rounded-xl flex items-center justify-center mb-6">
        <i class="fas fa-home text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Free Home Energy Audit</h3>
    <p class="text-gray-600 mb-4 leading-relaxed">
        Our certified energy experts conduct a comprehensive assessment...
    </p>
```

**To Update Feature Title**:
1. Find the `<h3>` tag in the feature card
2. Replace the text: `Free Home Energy Audit`
3. Example: `<h3 class="text-2xl font-bold text-gray-900 mb-4">Expert Energy Assessment</h3>`

**To Update Feature Description**:
1. Find the `<p>` tag with the description
2. Replace the entire paragraph text
3. Keep the class names: `class="text-gray-600 mb-4 leading-relaxed"`

**To Update Feature Icon**:
1. Find the `<i class="fas fa-home text-white text-2xl"></i>` line
2. Replace `fa-home` with another Font Awesome icon
3. Options: `fa-chart-bar`, `fa-clipboard`, `fa-cog`, `fa-star`
4. Example: `<i class="fas fa-chart-bar text-white text-2xl"></i>`

**To Update Feature Bullet Points**:
1. Find the `<ul>` (unordered list) within the feature card
2. Each bullet point is wrapped in `<li>` tags
3. Replace the text while keeping the structure:
```html
<ul class="space-y-3">
    <li class="flex items-start space-x-3">
        <i class="fas fa-check text-green-500 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Your new bullet point text</span>
    </li>
</ul>
```

**Repeat for all three feature cards** (lines 180-220, 222-261).

---

### Section 4: Benefits Section

Three main benefit cards plus four additional benefits.

#### **Updating Main Benefit Cards**

**Location**: Lines 280-340

**First Benefit Card (Lower Utility Costs)**:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-2xl hover:scale-105 transition-all duration-300 border border-gray-100">
    <div class="w-20 h-20 gradient-accent rounded-xl flex items-center justify-center mb-6 mx-auto">
        <i class="fas fa-dollar-sign text-white text-4xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4 text-center">Lower Utility Costs</h3>
    <p class="text-gray-600 mb-6 text-center leading-relaxed">
        Dramatically reduce your monthly electricity bills...
    </p>
    <div class="bg-purple-50 rounded-lg p-4 text-center">
        <p class="text-sm text-gray-600 mb-2">Average Annual Savings:</p>
        <p class="text-3xl font-bold text-purple-600">$2,400+</p>
    </div>
</div>
```

**To Update Benefit Title**:
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4 text-center">Your New Title</h3>
```

**To Update Benefit Description**:
```html
<p class="text-gray-600 mb-6 text-center leading-relaxed">
    Your new description text here.
</p>
```

**To Update the Statistics Box**:
```html
<div class="bg-purple-50 rounded-lg p-4 text-center">
    <p class="text-sm text-gray-600 mb-2">New Label:</p>
    <p class="text-3xl font-bold text-purple-600">New Value</p>
</div>
```

**To Update Benefit Icon**:
```html
<i class="fas fa-dollar-sign text-white text-4xl"></i>
```
Replace `fa-dollar-sign` with your chosen icon (e.g., `fa-home`, `fa-leaf`, `fa-chart-line`)

**Repeat for all three benefit cards** (lines 280-340).

#### **Updating Additional Benefits Grid**

**Location**: Lines 342-376

**Single Additional Benefit Structure**:
```html
<div class="flex items-start space-x-4">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-12 w-12 rounded-md gradient-accent">
            <i class="fas fa-shield-alt text-white"></i>
        </div>
    </div>
    <div>
        <h4 class="text-lg font-bold text-gray-900">Comprehensive Warranties</h4>
        <p class="text-gray-600 mt-2">25-year panel warranty, 10-year inverter warranty, and 10-year workmanship guarantee for complete peace of mind.</p>
    </div>
</div>
```

**To Update**:
1. Change the icon: `<i class="fas fa-shield-alt text-white"></i>`
2. Change the title: `<h4>Your New Title</h4>`
3. Change the description: `<p>Your new description</p>`

---

### Section 5: Testimonials Section

Four customer testimonial cards.

#### **Updating Testimonial Content**

**Location**: Lines 378-445

**Single Testimonial Structure**:
```html
<div class="bg-gradient-to-br from-gray-50 to-white rounded-2xl p-8 border border-gray-200 hover:shadow-xl hover:scale-105 transition-all duration-300">
    <div class="flex items-center space-x-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 mb-6 leading-relaxed">
        "The entire process was seamless from start to finish..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Jennifer Martinez</p>
        <p class="text-sm text-gray-600">Homeowner, Las Vegas</p>
    </div>
</div>
```

**To Update Testimonial Quote**:
1. Replace the text in the `<p class="text-gray-700 mb-6 leading-relaxed">` section
2. Keep the opening and closing quotation marks
3. Example:
```html
<p class="text-gray-700 mb-6 leading-relaxed">
    "Amazing service! They installed our system in just 2 days and we're already saving money."
</p>
```

**To Update Customer Name and Location**:
```html
<p class="font-bold text-gray-900">Your Customer Name</p>
<p class="text-sm text-gray-600">Their Title, City Name</p>
```

**To Change Star Rating**:
- To show 4 stars instead of 5, remove one star line:
```html
<div class="flex items-center space-x-1 mb-4">
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <!-- Remove this line to show 4 stars -->
</div>
```

---

### Section 6: About Us Section

Company information section.

#### **Updating About Us Text**

**Location**: Lines 477-491

**Current Structure**:
```html
<div class="space-y-8">
    <h2 class="text-4xl md:text-5xl font-bold leading-tight">About America's Home Contractors</h2>
    
    <p class="text-lg leading-relaxed text-gray-200">
        Founded in 2010, America's Home Contractors has been at the forefront...
    </p>

    <p class="text-lg leading-relaxed text-gray-200">
        Our mission is simple yet powerful...
    </p>
```

**To Update Heading**:
```html
<h2 class="text-4xl md:text-5xl font-bold leading-tight">About Your Company Name</h2>
```

**To Update Paragraphs**:
1. Replace the text in each `<p>` tag
2. Keep the class names: `class="text-lg leading-relaxed text-gray-200"`
3. You can add more paragraphs by copying and pasting the `<p>` tag

**To Update Statistics**:
```html
<div class="grid grid-cols-3 gap-4 pt-4">
    <div>
        <p class="text-3xl font-bold text-purple-400">2,500+</p>
        <p class="text-gray-300">Systems Installed</p>
    </div>
    <!-- Update the number and label -->
</div>
```

---

### Section 7: FAQ Section

Expandable frequently asked questions.

#### **Updating FAQ Questions and Answers**

**Location**: Lines 520-615

**Single FAQ Item Structure**:
```html
<div class="faq-item bg-gradient-to-br from-gray-50 to-white rounded-xl border border-gray-200 overflow-hidden hover:border-purple-300 transition-colors duration-300">
    <button class="faq-question w-full px-6 py-5 flex items-center justify-between text-left hover:bg-purple-50 transition-colors duration-300 cursor-pointer" aria-expanded="false">
        <span class="text-lg font-semibold text-gray-900">How much can I save with solar panels?</span>
        <i class="faq-icon fas fa-chevron-down text-purple-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 pb-5 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            The amount you save depends on several factors...
        </p>
    </div>
</div>
```

**To Update FAQ Question**:
1. Replace the text in the `<span>` inside the button:
```html
<span class="text-lg font-semibold text-gray-900">Your New Question?</span>
```

**To Update FAQ Answer**:
1. Replace the text in the `<p>` inside the `.faq-answer` div:
```html
<p class="text-gray-700 leading-relaxed">
    Your answer text here. You can make it as long as needed.
</p>
```

**To Add a New FAQ Item**:
1. Copy the entire FAQ item structure above
2. Paste it before the closing `</div>` of the FAQ section
3. Update the question and answer text
4. The JavaScript will automatically make it expandable

---

### Section 8: Footer

Bottom of the page with links and company information.

#### **Updating Footer Company Info**

**Location**: Lines 647-659

**Current Code**:
```html
<div>
    <div class="flex items-center space-x-2 mb-4">
        <div class="gradient-accent w-10 h-10 rounded-lg flex items-center justify-center">
            <i class="fas fa-sun text-white text-lg"></i>
        </div>
        <span class="text-xl font-bold text-white">SolarVegas</span>
    </div>
    <p class="text-gray-400 mb-6">
        Transforming Vegas homes with premium solar solutions since 2010.
    </p>
```

**To Update**:
1. Change logo text: `<span class="text-xl font-bold text-white">Your Company Name</span>`
2. Change description: `<p class="text-gray-400 mb-6">Your company description.</p>`

#### **Updating Footer Links**

**Location**: Lines 661-712

**Quick Links Section** (Lines 661-670):
```html
<div>
    <h4 class="text-white font-bold text-lg mb-6">Quick Links</h4>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
        <li><a href="#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
        <li><a href="#faq" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">FAQ</a></li>
    </ul>
</div>
```

**Legal Links Section** (Lines 672-681):
```html
<div>
    <h4 class="text-white font-bold text-lg mb-6">Legal</h4>
    <ul class="space-y-3">
        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Blog</a></li>
    </ul>
</div>
```

**Contact Info Section** (Lines 683-699):
```html
<div>
    <h4 class="text-white font-bold text-lg mb-6">Contact Us</h4>
    <ul class="space-y-4">
        <li class="flex items-start space-x-3">
            <i class="fas fa-map-marker-alt text-purple-400 mt-1 flex-shrink-0"></i>
            <span class="text-gray-400">Las Vegas, Nevada</span>
        </li>
        <li class="flex items-start space-x-3">
            <i class="fas fa-envelope text-purple-400 mt-1 flex-shrink-0"></i>
            <a href="mailto:x_n2deep_x@yahoo.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">x_n2deep_x@yahoo.com</a>
        </li>
        <li class="flex items-start space-x-3">
            <i class="fas fa-phone text-purple-400 mt-1 flex-shrink-0"></i>
            <span class="text-gray-400">1-800-SOLAR-VGS</span>
        </li>
    </ul>
</div>
```

---

## Modifying Tailwind CSS Classes

Tailwind CSS provides pre-made styling classes. Understanding how to modify them helps you customize colors, sizes, spacing, and more without writing custom CSS.

### Common Tailwind Classes in Your Landing Page

#### **Text Sizing**

| Class | Size | Used For |
|-------|------|----------|
| `text-sm` | Small | Secondary text, captions |
| `text-base` | Normal | Body text |
| `text-lg` | Large | Subheadings |
| `text-xl` | Extra Large | Section descriptions |
| `text-2xl` | 2x Large | Card titles |
| `text-3xl` | 3x Large | Statistics numbers |
| `text-4xl` | 4x Large | Section headings |
| `text-5xl` | 5x Large | Main headlines |
| `text-6xl` | 6x Large | Large hero text |

**Example**: Change a heading from `text-4xl` to `text-5xl`:
```html
<!-- Before -->
<h2 class="text-4xl md:text-5xl font-bold text-gray-900">Features</h2>

<!-- After -->
<h2 class="text-5xl md:text-6xl font-bold text-gray-900">Features</h2>
```

#### **Text Colors**

| Class | Color | Usage |
|-------|-------|-------|
| `text-white` | White | Light backgrounds |
| `text-gray-600` | Medium Gray | Body text |
| `text-gray-700` | Darker Gray | Emphasis text |
| `text-gray-900` | Very Dark Gray | Headlines |
| `text-purple-600` | Purple | Accent color |
| `text-green-500` | Green | Success/checkmarks |
| `text-yellow-400` | Yellow | Star ratings |

**Example**: Change text color from gray to purple:
```html
<!-- Before -->
<p class="text-gray-600">This is body text</p>

<!-- After -->
<p class="text-purple-600">This is body text</p>
```

#### **Background Colors**

| Class | Color | Usage |
|-------|-------|-------|
| `bg-white` | White | Card backgrounds |
| `bg-gray-50` | Very Light Gray | Section backgrounds |
| `bg-gray-100` | Light Gray | Hover states |
| `bg-purple-50` | Light Purple | Accent backgrounds |
| `bg-purple-600` | Dark Purple | Buttons |

**Example**: Change background color:
```html
<!-- Before -->
<div class="bg-white rounded-lg p-4">Content</div>

<!-- After -->
<div class="bg-gray-50 rounded-lg p-4">Content</div>
```

#### **Padding (Spacing Inside)**

| Class | Size | Effect |
|-------|------|--------|
| `p-2` | Small | 0.5rem padding all sides |
| `p-4` | Medium | 1rem padding all sides |
| `p-6` | Large | 1.5rem padding all sides |
| `p-8` | Extra Large | 2rem padding all sides |
| `px-4` | Horizontal | Left & right padding only |
| `py-4` | Vertical | Top & bottom padding only |

**Example**: Increase padding on a card:
```html
<!-- Before -->
<div class="p-6 rounded-lg">Card content</div>

<!-- After -->
<div class="p-8 rounded-lg">Card content</div>
```

#### **Margins (Spacing Outside)**

| Class | Size | Effect |
|-------|------|--------|
| `m-2` | Small | 0.5rem margin all sides |
| `m-4` | Medium | 1rem margin all sides |
| `mb-4` | Bottom | 1rem margin below element |
| `mt-2` | Top | 0.5rem margin above element |
| `mx-auto` | Horizontal Center | Centers element horizontally |

**Example**: Add space below a heading:
```html
<!-- Before -->
<h2 class="text-4xl font-bold">Our Features</h2>

<!-- After -->
<h2 class="text-4xl font-bold mb-8">Our Features</h2>
```

#### **Responsive Design Classes**

Your page uses responsive classes that change styling on different screen sizes:

| Prefix | Screen Size | Usage |
|--------|------------|-------|
| *(no prefix)* | Mobile (default) | Applies to all screen sizes |
| `sm:` | Small tablets (640px+) | Tablets and up |
| `md:` | Medium tablets (768px+) | Medium devices and up |
| `lg:` | Large desktops (1024px+) | Large screens and up |

**Example**: Different text sizes on different screens:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
    This text is 4xl on phones, 5xl on tablets, 6xl on desktops
</h1>
```

**Example**: Hide element on mobile, show on desktop:
```html
<!-- This image only shows on large screens (lg:) -->
<img src="image.jpg" alt="Description" class="hidden lg:block">
```

#### **Hover Effects**

Classes that trigger when you hover over an element:

| Class | Effect |
|-------|--------|
| `hover:text-purple-600` | Changes text color on hover |
| `hover:bg-purple-50` | Changes background color on hover |
| `hover:shadow-xl` | Adds shadow on hover |
| `hover:scale-105` | Slightly enlarges on hover |

**Example**: Make a button change color on hover:
```html
<button class="bg-purple-600 hover:bg-purple-700 text-white px-6 py-2 rounded-lg">
    Click Me
</button>
```

#### **Border Radius (Rounded Corners)**

| Class | Roundness |
|-------|-----------|
| `rounded` | Slightly rounded |
| `rounded-lg` | More rounded |
| `rounded-xl` | Very rounded |
| `rounded-2xl` | Extra rounded |
| `rounded-full` | Completely round (circles) |

**Example**: Make corners more rounded:
```html
<!-- Before -->
<div class="rounded-lg p-6">Card</div>

<!-- After -->
<div class="rounded-2xl p-6">Card</div>
```

#### **Shadow Effects**

| Class | Effect |
|-------|--------|
| `shadow` | Subtle shadow |
| `shadow-lg` | Medium shadow |
| `shadow-xl` | Large shadow |
| `shadow-2xl` | Extra large shadow |

**Example**: Add shadow to a card:
```html
<!-- Before -->
<div class="bg-white rounded-lg p-6">Card</div>

<!-- After -->
<div class="bg-white rounded-lg p-6 shadow-lg">Card</div>
```

### Modifying the Gradient Accent Colors

Your page uses a purple-to-blue gradient defined in the `<style>` section (lines 18-21):

```css
.gradient-accent {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

**To Change the Gradient**:
1. Find the `.gradient-accent` class in the `<style>` section
2. The colors are hex codes: `#667eea` (purple) and `#764ba2` (darker purple)
3. Replace with new hex codes:
```css
.gradient-accent {
    background: linear-gradient(135deg, #FF6B6B 0%, #FF8E53 100%);
}
```

**Common Gradient Combinations**:
- **Blue to Purple**: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`
- **Green to Teal**: `linear-gradient(135deg, #11998e 0%, #38ef7d 100%)`
- **Orange to Red**: `linear-gradient(135deg, #ff6b6b 0%, #ee5a6f 100%)`
- **Pink to Purple**: `linear-gradient(135deg, #f093fb 0%, #f5576c 100%)`

### Practical Examples: Making Common Changes

#### **Example 1: Make All Headings Larger**

Find all `<h2>` tags and change:
```html
<!-- Before -->
<h2 class="text-4xl md:text-5xl font-bold">Section Title</h2>

<!-- After -->
<h2 class="text-5xl md:text-6xl font-bold">Section Title</h2>
```

#### **Example 2: Change Button Color Scheme**

Find the `.btn-primary` class in the `<style>` section (lines 31-37):
```css
/* Before */
.btn-primary {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    transition: all 0.3s ease;
}

/* After */
.btn-primary {
    background: linear-gradient(135deg, #FF6B6B 0%, #FF8E53 100%);
    transition: all 0.3s ease;
}
```

#### **Example 3: Increase Card Padding**

Find feature cards and change:
```html
<!-- Before -->
<div class="feature-card bg-gradient-to-br from-gray-50 to-white rounded-2xl p-8">

<!-- After -->
<div class="feature-card bg-gradient-to-br from-gray-50 to-white rounded-2xl p-12">
```

#### **Example 4: Make Text More Visible**

Change text color to darker:
```html
<!-- Before -->
<p class="text-gray-600">Description text</p>

<!-- After -->
<p class="text-gray-800">Description text</p>
```

---

## Fixing and Updating Links

Links are crucial for navigation. Your page has several types of links that need proper maintenance.

### Understanding Link Types

**Internal Links** (within your website):
- Point to sections on the same page using `#` (hash symbol)
- Example: `href="#features"` jumps to the Features section
- Example: `href="privacy.html"` goes to privacy page in same folder

**External Links** (outside your website):
- Use full URL with `https://`
- Example: `href="https://americashomecontractors.com/actnow"`

**Email Links**:
- Use `mailto:` format
- Example: `href="mailto:email@example.com"`

**Phone Links**:
- Use `tel:` format
- Example: `href="tel:+1-800-555-1234"`

### All Links in Your Landing Page

Here's a complete list of every link in your page and where to find it:

#### **Header Navigation Links**

**Location**: Lines 59-65 (Desktop) and 75-82 (Mobile)

| Link Text | Current href | Type | Purpose |
|-----------|-------------|------|---------|
| Features | `#features` | Internal | Jumps to Features section |
| Benefits | `#benefits` | Internal | Jumps to Benefits section |
| Testimonials | `#testimonials` | Internal | Jumps to Testimonials section |
| FAQ | `#faq` | Internal | Jumps to FAQ section |
| Get Started | `https://americashomecontractors.com/actnow` | External | Main CTA button |

#### **Hero Section Buttons**

**Location**: Lines 133-139

| Button Text | Current href | Type |
|-------------|-------------|------|
| Get Your Free Energy Audit | `https://americashomecontractors.com/actnow` | External |
| Learn More | (no href - it's a button) | N/A |

#### **CTA Section Button**

**Location**: Line 635

| Button Text | Current href | Type |
|-------------|-------------|------|
| Claim Your Free Energy Audit Now | `https://americashomecontractors.com/actnow` | External |

#### **Footer Links**

**Location**: Lines 661-699

| Link Text | Current href | Type | Location |
|-----------|-------------|------|----------|
| Features | `#features` | Internal | Quick Links |
| Benefits | `#benefits` | Internal | Quick Links |
| Testimonials | `#testimonials` | Internal | Quick Links |
| FAQ | `#faq` | Internal | Quick Links |
| Privacy Policy | `privacy.html` | Internal | Legal |
| Terms of Service | `terms.html` | Internal | Legal |
| Blog | `blog.html` | Internal | Legal |
| Email | `mailto:x_n2deep_x@yahoo.com` | Email | Contact Info |
| Phone | (text only) | N/A | Contact Info |

### Step-by-Step: Updating Links

#### **Step 1: Update Your Main CTA Link (Most Important)**

This is the link that appears in multiple places and directs people to your contact/booking page.

**Find All Instances**:
1. Line 65: Desktop "Get Started" button
2. Line 82: Mobile "Get Started" button
3. Line 138: Hero "Get Your Free Energy Audit" button
4. Line 635: Final CTA section button

**Current Code Example** (Line 65):
```html
<a href="https://americashomecontractors.com/actnow" class="btn-primary text-white px-6 py-2 rounded-lg font-semibold">Get Started</a>
```

**To Update**:
1. Replace `https://americashomecontractors.com/actnow` with your URL
2. Example: `https://yourwebsite.com/contact`
3. Or: `https://yourwebsite.com/free-consultation`
4. **Important**: Update ALL four instances (lines 65, 82, 138, 635)

**Complete Example**:
```html
<!-- Before -->
<a href="https://americashomecontractors.com/actnow" class="btn-primary text-white px-6 py-2 rounded-lg font-semibold">Get Started</a>

<!-- After -->
<a href="https://yourcompany.com/schedule-audit" class="btn-primary text-white px-6 py-2 rounded-lg font-semibold">Get Started</a>
```

#### **Step 2: Update Footer Contact Email**

**Location**: Line 690

**Current Code**:
```html
<a href="mailto:x_n2deep_x@yahoo.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">x_n2deep_x@yahoo.com</a>
```

**To Update**:
1. Replace `x_n2deep_x@yahoo.com` with your email (appears twice - in href and as link text)
2. Example:
```html
<a href="mailto:info@yourcompany.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">info@yourcompany.com</a>
```

#### **Step 3: Update Footer Phone Number**

**Location**: Line 695

**Current Code**:
```html
<span class="text-gray-400">1-800-SOLAR-VGS</span>
```

**To Update**:
1. Replace the phone number with yours
2. Example:
```html
<span class="text-gray-400">1-800-555-1234</span>
```

**Optional - Make Phone Number Clickable**:
```html
<!-- Before (text only) -->
<span class="text-gray-400">1-800-555-1234</span>

<!-- After (clickable) -->
<a href="tel:+1-800-555-1234" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">1-800-555-1234</a>
```

#### **Step 4: Update Footer Address**

**Location**: Line 687

**Current Code**:
```html
<span class="text-gray-400">Las Vegas, Nevada</span>
```

**To Update**:
1. Replace with your address
2. Example:
```html
<span class="text-gray-400">123 Solar Street, Las Vegas, NV 89101</span>
```

#### **Step 5: Update Footer Company Name**

**Location**: Line 680

**Current Code**:
```html
<p class="text-gray-400 mb-6">
    Transforming Vegas homes with premium solar solutions since 2010.
</p>
```

**To Update**:
1. Replace the tagline with yours
2. Example:
```html
<p class="text-gray-400 mb-6">
    Your company name - premium solar energy solutions for Nevada homes.
</p>
```

#### **Step 6: Verify Internal Links Work**

Internal links (those starting with `#`) should match section IDs. Verify these exist:

**Check these sections have correct IDs**:
1. Line 180: `<section id="features">` - matches `href="#features"`
2. Line 263: `<section id="benefits">` - matches `href="#benefits"`
3. Line 378: `<section id="testimonials">` - matches `href="#testimonials"`
4. Line 493: `<section id="faq">` - matches `href="#faq"`

If a section is missing its `id`, links won't work. Example fix:
```html
<!-- Before - missing id -->
<section class="py-24 bg-white">

<!-- After - has id -->
<section id="features" class="py-24 bg-white">
```

### Common Link Problems & Solutions

#### **Problem 1: Link Goes to Wrong Page**

**Symptom**: Clicking a link takes you somewhere unexpected

**Solution**:
1. Check the `href` value is correct
2. Ensure external URLs start with `https://`
3. Ensure internal page links end with `.html`

```html
<!-- Wrong -->
<a href="contact">Contact Us</a>

<!-- Correct -->
<a href="contact.html">Contact Us</a>
```

#### **Problem 2: External Link Doesn't Work**

**Symptom**: Clicking external link shows error

**Solution**:
1. Verify the full URL is correct
2. Test the URL in your browser first
3. Ensure it starts with `https://`

```html
<!-- Wrong -->
<a href="americashomecontractors.com/actnow">

<!-- Correct -->
<a href="https://americashomecontractors.com/actnow">
```

#### **Problem 3: Internal Section Link Doesn't Work**

**Symptom**: Clicking "Features" link doesn't jump to Features section

**Solution**:
1. Check the section has an `id` attribute
2. Verify the href `#name` matches the `id="name"`

```html
<!-- Wrong - section missing id -->
<section class="py-24">
    <h2>Features</h2>
</section>

<!-- Correct -->
<section id="features" class="py-24">
    <h2>Features</h2>
</section>
```

#### **Problem 4: Email Link Doesn't Work**

**Symptom**: Clicking email link doesn't open email client

**Solution**:
1. Ensure link uses `mailto:` format
2. Check email address is spelled correctly

```html
<!-- Wrong -->
<a href="x_n2deep_x@yahoo.com">Email Us</a>

<!-- Correct -->
<a href="mailto:x_n2deep_x@yahoo.com">Email Us</a>
```

---

## Adding Privacy and Terms Pages

Your footer currently links to `privacy.html` and `terms.html` pages that don't exist yet. This guide will help you create them.

### Step 1: Create the Privacy Policy Page

#### **Create a New File**

1. In your file manager or code editor, create a new file
2. Name it exactly: `privacy.html`
3. Save it in the same folder as your `index.html`

#### **Copy This Template**

Here's a complete privacy policy template you can customize:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for SolarVegas">
    <title>Privacy Policy - SolarVegas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-800">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center">
                <div class="flex items-center space-x-2">
                    <div class="bg-gradient-to-r from-purple-600 to-purple-800 w-10 h-10 rounded-lg flex items-center justify-center">
                        <i class="fas fa-sun text-white text-lg"></i>
                    </div>
                    <span class="text-xl font-bold text-gray-900">SolarVegas</span>
                </div>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-24 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold text-gray-900 mb-4">Privacy Policy</h1>
            <p class="text-gray-600 mb-12">Last updated: January 2025</p>

            <div class="bg-white rounded-lg p-8 shadow-lg space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        America's Home Contractors ("we," "us," "our," or "Company") operates the SolarVegas website. This Privacy Policy explains how we collect, use, disclose, and otherwise handle your information when you visit our website, use our services, or interact with us.
                    </p>
                    <p class="text-gray-700 leading-relaxed">
                        We are committed to protecting your privacy and ensuring you have a positive experience on our website. Please read this Privacy Policy carefully to understand our privacy practices.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <h3 class="text-lg font-semibold text-gray-800 mb-3">Personal Information</h3>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We collect personal information that you voluntarily provide to us, including:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 mb-6">
                        <li>Name and contact information (email, phone number, address)</li>
                        <li>Information about your home and energy usage</li>
                        <li>Billing and payment information</li>
                        <li>Any other information you choose to provide</li>
                    </ul>

                    <h3 class="text-lg font-semibold text-gray-800 mb-3">Automatically Collected Information</h3>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        When you visit our website, we automatically collect certain information, including:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>Browser type and operating system</li>
                        <li>IP address and device identifiers</li>
                        <li>Pages visited and time spent on our website</li>
                        <li>Referring website and exit pages</li>
                        <li>Click stream data and other usage information</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How We Use Your Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We use the information we collect for various purposes, including:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>Providing and improving our solar energy services</li>
                        <li>Responding to your inquiries and requests</li>
                        <li>Processing transactions and sending related information</li>
                        <li>Sending marketing communications (with your consent)</li>
                        <li>Analyzing website usage and trends</li>
                        <li>Detecting and preventing fraud</li>
                        <li>Complying with legal obligations</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Information Sharing</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We do not sell, trade, or rent your personal information to third parties. We may share your information with:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>Service providers who assist us in operating our website and business</li>
                        <li>Legal authorities when required by law</li>
                        <li>Business partners with your consent</li>
                        <li>Your explicit permission</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Data Security</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet or electronic storage is completely secure. While we strive to use commercially acceptable means to protect your information, we cannot guarantee absolute security.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Your Rights and Choices</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        You have the right to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>Access the personal information we hold about you</li>
                        <li>Request correction of inaccurate information</li>
                        <li>Request deletion of your information</li>
                        <li>Opt-out of marketing communications</li>
                        <li>Withdraw your consent at any time</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Cookies and Tracking</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Our website may use cookies and similar tracking technologies to enhance your experience. You can control cookie settings through your browser preferences. Note that disabling cookies may affect website functionality.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Third-Party Links</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Our website may contain links to third-party websites. We are not responsible for the privacy practices of these external sites. We encourage you to review their privacy policies before providing any personal information.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Children's Privacy</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Our website is not intended for children under 13 years old. We do not knowingly collect personal information from children. If we become aware that we have collected information from a child under 13, we will take steps to delete such information and terminate the child's account.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Changes to This Privacy Policy</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We may update this Privacy Policy from time to time to reflect changes in our practices or for other operational, legal, or regulatory reasons. We will notify you of any material changes by posting the updated Privacy Policy on our website and updating the "Last updated" date.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">11. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                    </p>
                    <div class="bg-gray-50 p-4 rounded-lg">
                        <p class="text-gray-700"><strong>America's Home Contractors</strong></p>
                        <p class="text-gray-700">Email: <a href="mailto:x_n2deep_x@yahoo.com" class="text-purple-600 hover:text-purple-800">x_n2deep_x@yahoo.com</a></p>
                        <p class="text-gray-700">Phone: 1-800-SOLAR-VGS</p>
                        <p class="text-gray-700">Location: Las Vegas, Nevada</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; 2025 America's Home Contractors. All rights reserved.
                </p>
                <div class="flex justify-center space-x-6">
                    <a href="index.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

#### **Create a New File**

1. Create a new file named exactly: `terms.html`
2. Save it in the same folder as your `index.html`

#### **Copy This Template**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for SolarVegas">
    <title>Terms of Service - SolarVegas</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-800">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center">
                <div class="flex items-center space-x-2">
                    <div class="bg-gradient-to-r from-purple-600 to-purple-800 w-10 h-10 rounded-lg flex items-center justify-center">
                        <i class="fas fa-sun text-white text-lg"></i>
                    </div>
                    <span class="text-xl font-bold text-gray-900">SolarVegas</span>
                </div>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-purple-600 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Terms of Service Content -->
    <section class="py-24 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl font-bold text-gray-900 mb-4">Terms of Service</h1>
            <p class="text-gray-600 mb-12">Last updated: January 2025</p>

            <div class="bg-white rounded-lg p-8 shadow-lg space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Acceptance of Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        By accessing and using the SolarVegas website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service. America's Home Contractors reserves the right to modify these Terms of Service at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on SolarVegas for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                        <li>Violating any applicable laws or regulations</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials on SolarVegas are provided on an 'as is' basis. America's Home Contractors makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall America's Home Contractors or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on SolarVegas, even if America's Home Contractors or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials appearing on SolarVegas could include technical, typographical, or photographic errors. America's Home Contractors does not warrant that any of the materials on its website are accurate, complete, or current. America's Home Contractors may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p class="text-gray-700 leading-relaxed">
                        America's Home Contractors has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by America's Home Contractors of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p class="text-gray-700 leading-relaxed">
                        America's Home Contractors may revise these Terms of Service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these Terms of Service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These Terms of Service and any separate agreements we provide to render services shall be governed by and construed in accordance with the laws of the State of Nevada, United States, without regard to its conflict of law provisions.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. User Responsibilities</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        As a user of our website and services, you agree to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>Provide accurate and complete information</li>
                        <li>Maintain the confidentiality of your account information</li>
                        <li>Notify us immediately of any unauthorized use of your account</li>
                        <li>Comply with all applicable laws and regulations</li>
                        <li>Not engage in any unlawful or prohibited activities</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Service Warranties</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        America's Home Contractors warrants that:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700">
                        <li>All solar installations are performed by certified technicians</li>
                        <li>Products used meet industry standards and regulations</li>
                        <li>Work is performed in a professional and workmanlike manner</li>
                        <li>All warranties provided are honored as stated</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">11. Limitation of Liability</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall America's Home Contractors be liable for any indirect, incidental, special, consequential, or punitive damages, or any loss of revenue or profits, whether incurred directly or indirectly, arising from the use of or inability to use the website or services.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">12. Contact Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <div class="bg-gray-50 p-4 rounded-lg">
                        <p class="text-gray-700"><strong>America's Home Contractors</strong></p>
                        <p class="text-gray-700">Email: <a href="mailto:x_n2deep_x@yahoo.com" class="text-purple-600 hover:text-purple-800">x_n2deep_x@yahoo.com</a></p>
                        <p class="text-gray-700">Phone: 1-800-SOLAR-VGS</p>
                        <p class="text-gray-700">Location: Las Vegas, Nevada</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; 2025 America's Home Contractors. All rights reserved.
                </p>
                <div class="flex justify-center space-x-6">
                    <a href="index.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Verify Your File Structure

After creating both files, your folder should look like this:

```
your-project-folder/
├── index.html          (your main landing page)
├── privacy.html        (new privacy policy)
├── terms.html          (new terms of service)
└── (any other files)
```

### Step 4: Test the Links

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - should open `privacy.html`
4. Click on "Terms of Service" - should open `terms.html`
5. Click the back link "← Back to Home" on either page - should return to `index.html`

### Step 5: Customize the Policy Pages

Both policy pages are templates. Update them with your specific information:

#### **In privacy.html, update**:
- Company name (replace "America's Home Contractors")
- Email address (replace "x_n2deep_x@yahoo.com")
- Phone number (replace "1-800-SOLAR-VGS")
- Address (replace "Las Vegas, Nevada")
- Last updated date (line 13)
- Any specific privacy practices relevant to your business

#### **In terms.html, update**:
- Company name (replace "America's Home Contractors")
- Email address (replace "x_n2deep_x@yahoo.com")
- Phone number (replace "1-800-SOLAR-VGS")
- Address (replace "Las Vegas, Nevada")
- Last updated date (line 13)
- State/jurisdiction (currently "Nevada" on line 113)
- Any specific terms relevant to your services

### Step 6: Create a Blog Page (Optional)

The footer also links to `blog.html`. If you want to create it, follow the same pattern:

1. Create a new file named `blog.html`
2. Use the privacy.html or terms.html template as a starting point
3. Replace the content with blog articles
4. Update all links in the footer to point to `blog.html`

If you don't want a blog page, remove the blog link from the footer:

```html
<!-- Remove this line from footer -->
<li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Blog</a></li>
```

---

## Troubleshooting Guide

### Common Issues and Solutions

#### **Issue 1: Links Don't Work**

**Problem**: Clicking a link does nothing or shows an error

**Causes and Solutions**:

1. **Internal section links not working**
   - **Check**: Does the section have an `id` attribute?
   - **Example**: `<section id="features">` for link `href="#features"`
   - **Fix**: Add missing `id` to section

2. **Page links not working**
   - **Check**: Is the filename exactly correct (including `.html`)?
   - **Example**: `href="privacy.html"` not `href="privacy"` or `href="Privacy.html"`
   - **Fix**: Verify exact filename matches

3. **External links not working**
   - **Check**: Does URL start with `https://`?
   - **Fix**: Add `https://` if missing
   - **Example**: `href="https://americashomecontractors.com/actnow"`

#### **Issue 2: Page Layout Looks Wrong**

**Problem**: Elements are misaligned, colors are off, or spacing is incorrect

**Causes and Solutions**:

1. **Accidental class deletion**
   - **Check**: Are all classes still in the `class=""` attribute?
   - **Fix**: Restore deleted classes from original code
   - **Example**: `<div class="bg-white rounded-lg p-8">` not `<div class="p-8">`

2. **Tailwind CSS not loading**
   - **Check**: Is the CDN link present? (Line 11: `<script src="https://cdn.tailwindcss.com"></script>`)
   - **Fix**: Ensure CDN link is not deleted
   - **Note**: If using offline, you'll need to compile Tailwind CSS locally

3. **Font Awesome icons not showing**
   - **Check**: Is Font Awesome link present? (Line 12: `<link rel="stylesheet" href="...font-awesome...">`)
   - **Fix**: Ensure CDN link is not deleted
   - **Symptom**: Icons appear as boxes or don't show

#### **Issue 3: Mobile Menu Doesn't Work**

**Problem**: Mobile hamburger menu doesn't open on phones

**Causes and Solutions**:

1. **JavaScript not running**
   - **Check**: Is the JavaScript section still at bottom of file? (Lines 721-800)
   - **Fix**: Ensure JavaScript code is not deleted
   - **Verify**: Check browser console for errors (F12 key)

2. **Mobile menu button not clickable**
   - **Check**: Is the button element still present? (Line 71)
   - **Fix**: Ensure button HTML is intact

#### **Issue 4: FAQ Accordion Doesn't Expand**

**Problem**: Clicking FAQ questions doesn't expand answers

**Causes and Solutions**:

1. **JavaScript missing**
   - **Check**: Is JavaScript code present at bottom of file?
   - **Fix**: Ensure FAQ JavaScript section (lines 777-797) is not deleted

2. **Wrong class names**
   - **Check**: Do elements have classes `faq-item`, `faq-question`, `faq-answer`?
   - **Fix**: Verify class names match exactly

#### **Issue 5: Text Doesn't Display Correctly**

**Problem**: Text is too small, too large, or wrong color

**Causes and Solutions**:

1. **Incorrect text size class**
   - **Current**: `text-lg` (large)
   - **Options**: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, etc.
   - **Fix**: Replace with appropriate size

2. **Wrong text color**
   - **Current**: `text-gray-600`
   - **Options**: `text-gray-700`, `text-gray-900`, `text-purple-600`, etc.
   - **Fix**: Replace with appropriate color

3. **Text not bold**
   - **Add**: `font-bold` to class list
   - **Example**: `class="text-lg font-bold"`

#### **Issue 6: Images Don't Show**

**Problem**: Image placeholders appear instead of actual images

**Causes and Solutions**:

1. **Image URL broken**
   - **Check**: Is the image URL (href) correct?
   - **Current**: Uses Unsplash URLs (free image service)
   - **Fix**: Replace with your own image URL
   - **Example**: `src="https://example.com/my-image.jpg"`

2. **Image file missing**
   - **If using local files**: Ensure image is in same folder as HTML
   - **Fix**: Use full URL path
   - **Example**: `src="images/my-photo.jpg"` (if images folder exists)

3. **Wrong image format**
   - **Supported**: `.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`
   - **Fix**: Ensure file extension is correct

#### **Issue 7: Button Colors Don't Change**

**Problem**: Buttons still show old colors after editing

**Causes and Solutions**:

1. **Editing wrong element**
   - **Check**: Are you editing the correct button?
   - **Note**: There are 4 main CTA buttons (lines 65, 82, 138, 635)
   - **Fix**: Update all instances

2. **Gradient color not changing**
   - **Check**: Is the gradient defined in `<style>` section?
   - **Location**: Lines 18-21 (`.gradient-accent`)
   - **Fix**: Update hex color codes in gradient definition

#### **Issue 8: Page Won't Load**

**Problem**: Page shows blank or error message

**Causes and Solutions**:

1. **HTML syntax error**
   - **Check**: Are all tags properly closed?
   - **Fix**: Ensure every `<tag>` has matching `</tag>`
   - **Example**: `<div>content</div>` not `<div>content`

2. **Missing closing tag**
   - **Check**: Look for unclosed tags
   - **Fix**: Add missing closing tag
   - **Example**: Missing `</div>` at end of section

3. **Invalid character in code**
   - **Check**: Did you accidentally delete important code?
   - **Fix**: Restore from original file

### How to Use Browser Developer Tools

When troubleshooting, use your browser's developer tools:

1. **Open Developer Tools**: Press `F12` or `Ctrl+Shift+I` (Windows) / `Cmd+Option+I` (Mac)
2. **Check Console**: Look for red error messages
3. **Inspect Elements**: Right-click element → "Inspect" to see HTML/CSS
4. **Check Network**: See if images/resources are loading

---

## Best Practices

### 1. Keep Backups

**Before making changes**:
1. Save a copy of your original `index.html` as `index-backup.html`
2. Use version control (Git) if possible
3. Keep dated backups of major changes

### 2. Update Consistently

**When changing information**:
- Update ALL instances, not just one
- Example: If you change your phone number, update it in:
  - Footer (line 695)
  - Anywhere else it appears

### 3. Test After Changes

**After every edit**:
1. Save the file
2. Refresh your browser (Ctrl+R or Cmd+R)
3. Check that changes appear correctly
4. Test all links work
5. Test on mobile (use browser's responsive mode - F12)

### 4. Maintain Responsive Design

**When adding content**:
- Use existing responsive classes (`md:`, `lg:`)
- Test on phones, tablets, and desktops
- Don't remove responsive prefixes
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

### 5. Keep Styling Consistent

**When modifying styles**:
- Use existing color palette (purples, grays)
- Maintain font sizes relationships
- Keep spacing consistent with other sections
- Don't mix different style approaches

### 6. Validate HTML

**Before deploying**:
1. Use [W3C Validator](https://validator.w3.org/)
2. Check for HTML errors
3. Fix any warnings

### 7. Test All Functionality

**Before going live**:
- [ ] All links work (internal and external)
- [ ] Mobile menu opens/closes
- [ ] FAQ accordion expands/collapses
- [ ] Forms submit (if applicable)
- [ ] Images load
- [ ] Page loads on different browsers
- [ ] Page loads on mobile devices

### 8. Optimize Images

**For faster loading**:
- Use compressed images (tools: TinyPNG, ImageOptim)
- Use appropriate file formats (.jpg for photos, .png for graphics)
- Specify image dimensions to prevent layout shift
- Use `alt` text for accessibility

### 9. Update Meta Tags

**For SEO and sharing**:
- Update page title (Line 10)
- Update meta description (Line 8)
- Update meta keywords (Line 9)
- Update Open Graph tags if sharing on social media

### 10. Accessibility Considerations

**Make your page inclusive**:
- Always include `alt` text on images
- Use semantic HTML (`<section>`, `<nav>`, `<footer>`)
- Ensure color contrast is sufficient
- Make links descriptive (not "click here")
- Test with keyboard navigation

---

## Quick Reference Checklist

Use this checklist when making updates:

### Content Updates
- [ ] Updated company name and logo
- [ ] Updated hero headline and subheading
- [ ] Updated all CTA button links (4 instances)
- [ ] Updated feature titles and descriptions
- [ ] Updated benefit cards
- [ ] Updated testimonials
- [ ] Updated about us section
- [ ] Updated FAQ questions and answers
- [ ] Updated footer contact information

### Link Updates
- [ ] Updated main CTA links (lines 65, 82, 138, 635)
- [ ] Updated email link (line 690)
- [ ] Updated phone number (line 695)
- [ ] Updated footer address (line 687)
- [ ] Verified all internal links work (#features, #benefits, etc.)
- [ ] Created privacy.html and terms.html pages
- [ ] Tested all links

### Styling Updates
- [ ] Updated gradient colors if needed
- [ ] Updated text colors if needed
- [ ] Updated button styling if needed
- [ ] Tested on mobile devices
- [ ] Tested on desktop browsers

### Final Checks
- [ ] Tested all links
- [ ] Tested mobile menu
- [ ] Tested FAQ accordion
- [ ] Tested on different browsers
- [ ] Tested on mobile devices
- [ ] Verified images load
- [ ] Checked HTML for errors
- [ ] Backed up original files

---

## Additional Resources

### Tools You Might Need

| Tool | Purpose | Website |
|------|---------|---------|
| Visual Studio Code | Code editor | https://code.visualstudio.com |
| Tailwind CSS | Styling framework | https://tailwindcss.com |
| Font Awesome | Icons | https://fontawesome.com |
| Unsplash | Free images | https://unsplash.com |
| TinyPNG | Image compression | https://tinypng.com |
| W3C Validator | HTML validation | https://validator.w3.org |
| Chrome DevTools | Browser debugging | F12 key |

### Learning Resources

- **HTML Basics**: [MDN HTML Guide](https://developer.mozilla.org/en-US/docs/Web/HTML)
- **Tailwind CSS**: [Tailwind Documentation](https://tailwindcss.com/docs)
- **Font Awesome Icons**: [Icon Library](https://fontawesome.com/icons)
- **Web Accessibility**: [WCAG Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

---

## Support

If you encounter issues not covered in this guide:

1. **Check the HTML Structure**: Ensure all tags are properly closed
2. **Verify File Names**: Ensure exact spelling and `.html` extension
3. **Clear Browser Cache**: Press `Ctrl+Shift+Delete` to clear cache
4. **Use Browser DevTools**: Press `F12` to check for errors
5. **Restore from Backup**: If major issues occur, restore original file

---

## Conclusion

You now have a comprehensive guide for maintaining and customizing your SolarVegas landing page. Remember to:

- Always back up your files before making major changes
- Test thoroughly after each update
- Keep styling and content consistent
- Update information across all instances
- Test on multiple devices and browsers

For questions about specific HTML or CSS concepts, refer to the sections above or consult the learning resources provided.

Happy editing! 🌞