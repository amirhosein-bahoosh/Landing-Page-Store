# Responsive Store Website

A responsive e-commerce-style website built with **HTML and CSS**, with a strong focus on **Flexbox, responsive design, media queries, and mobile-first development**.

This project was also a learning experience for understanding how different layouts should be structured and maintained across mobile, tablet, and desktop screen sizes.

## 📱 Responsive Navigation

The navigation bar changes depending on the screen size.

### Mobile

* Uses a mobile-first navigation structure.
* Includes a menu icon that rotates when interacted with.
* Clicking the menu icon displays the navigation list.
* The **Home** item also contains a secondary list.
* The mobile navigation contains text-based menu items.
* The logo is hidden on mobile.

### Tablet

* A separate tablet navigation structure is used.
* A **user/account icon** is added.
* The logo becomes visible.
* Navigation elements are adjusted specifically for tablet dimensions.

### Desktop

* A separate desktop navigation structure is used.
* The desktop version contains additional elements inside the search, account, and logo sections.
* Some elements that exist in the desktop layout are hidden on smaller screen sizes.
* The desktop navigation focuses more on icons and visual elements rather than displaying all menu text.

## 📐 Responsive Layout

The project uses **Flexbox** as the main layout system.

Different navigation structures were created for:

* Mobile
* Tablet
* Desktop

CSS media queries are used to control which version is visible at different breakpoints.

One of the main lessons from this project was that simply copying a mobile layout into a media query and modifying it for larger screens can quickly become difficult to maintain.

A better approach is to:

1. Keep styles shared between all screen sizes outside media queries.
2. Give each responsive section appropriate and clearly separated class names.
3. Keep mobile, tablet, and desktop-specific styles inside their relevant media queries.
4. Avoid reusing tablet-specific classes inside the desktop HTML structure.

## 🎨 Responsive Background

The hero section uses a responsive background image.

I used CSS `clamp()` for the background sizing and the padding of the content inside the hero section.

This allows the content and background image to grow more naturally as the viewport becomes wider.

The goal was to keep the following elements visually synchronized:

* Background image size
* Hero content
* Headings
* Paragraphs
* Internal spacing

The hero section's height is also adjusted according to the responsive size of the background image, allowing the section to scale more naturally across different screen sizes.

## 🖼️ Image Transformations

CSS `transform: rotate()` is used to rotate the watch image inside the banner by approximately **15 degrees**.

One useful CSS lesson from this project was that `transform` does not behave as expected on normal inline elements.

When transformations need to be applied reliably, the element should generally be changed to an appropriate display type such as:

```css
display: block;
```

or

```css
display: inline-block;
```

## 🧭 Mobile-First Approach

The project started with a **mobile-first CSS approach**.

Initially, I wrote the mobile navigation and then tried to adapt it for tablet and desktop using media queries.

During development, I realized that a more maintainable structure was to separate the navigation into three dedicated sections:

```text
Mobile Navbar
Tablet Navbar
Desktop Navbar
```

This made it easier to control the layout and visibility of each version independently.

## 💡 Lessons Learned

This project helped me understand several important concepts in responsive web development:

* How to structure layouts with **Flexbox**
* How to implement a **mobile-first workflow**
* How to use **media queries** effectively
* How to use `clamp()` for responsive sizing
* How to create different navigation structures for different breakpoints
* How background images can be scaled responsively
* How `transform` behaves differently depending on an element's display type
* Why shared CSS rules should be separated from breakpoint-specific rules
* Why responsive HTML structures should have appropriate class names for their specific components
* How copying an existing responsive component without updating its class names can cause unexpected layout conflicts

## 🔧 Main Technologies

* HTML5
* CSS3
* Flexbox
* Media Queries
* CSS `clamp()`
* CSS `transform`

## 📚 Project Purpose

The main purpose of this project was not only to create an e-commerce-style interface, but also to practice building a **responsive layout from scratch** and understand how HTML structure and CSS architecture affect the behavior of a website across different screen sizes.

The project represents a practical step in learning how to build cleaner, more maintainable responsive interfaces.

