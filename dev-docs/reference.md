

---
# High Level Context
## context
**Last Updated at:** 8/6/2024, 4:20:14 PM

Based on the overviews of all the SCSS files in this folder, here's a high-level overview of the folder's purpose and functionality:

This folder contains a collection of SCSS (Sass) files that form the core styling system for a Docusaurus-based documentation website. The purpose of this folder is to provide a comprehensive, customizable, and modular approach to styling various components and layouts of the documentation site.

Key aspects of this styling system include:

1. Theming: It implements both light and dark themes, allowing for seamless switching between color modes.

2. Component-specific styling: Individual files target specific components like the navbar, sidebar, footer, and search bar, allowing for easy customization of each element.

3. Typography: It defines consistent typography rules for headings, paragraphs, and other text elements across the site.

4. Responsive design: The styles are built with responsiveness in mind, ensuring the site looks good on various screen sizes and devices.

5. Custom components: It includes styles for custom components like cards, buttons, and tables, enhancing the visual appeal and functionality of the documentation.

6. Code highlighting: Special attention is given to styling code blocks and syntax highlighting for better readability.

7. Utility classes: It incorporates Tailwind CSS utility classes, providing a flexible system for rapid UI development.

8. Animations and effects: The system includes custom animations, transitions, and effects like glassmorphism to enhance user experience.

9. Customizability: Each file is structured to allow easy customization, with clear sections for colors, layouts, and component-specific styles.

10. Integration with Docusaurus: The styles are tailored to work seamlessly with Docusaurus-specific elements and classes.

Overall, this folder serves as a central hub for all styling needs of the Docusaurus template, providing a flexible and powerful system that can be easily adapted to various branding and design requirements while maintaining consistency and user-friendliness across the documentation site.

# Table of Contents (table-of-contents.scss)

## Overview

This SCSS file contains custom styles for the Table of Contents component in a Docusaurus theme. It modifies the appearance and behavior of both the mobile and desktop versions of the table of contents, enhancing the user experience and visual appeal.

Key features include:

1. Removal of default background styles for collapsible buttons
2. Custom styling for the "On This Page" header in the desktop version
3. Consistent font styling for table of contents links
4. Custom hover and active states for links
5. (Commented out) Styles for adding visual indicators to active links and applying backdrop filters

## How can I customize this for my usecase

To customize this file for your specific needs, you can modify various aspects of the styles:

1. **Collapsible Button Styles**: 
   If you want to change the appearance of the collapsible buttons, modify the `.tocCollapsibleButton_node_modules-\@docusaurus-theme-classic-lib-theme-TOCCollapsible-CollapseButton-styles-module::after` and `.theme-doc-toc-mobile .tocCollapsibleButton_TO0P:after` selectors.

2. **"On This Page" Header**:
   To change the text, font, or styling of the "On This Page" header, edit the `.theme-doc-toc-desktop::before` selector. You can modify the `content`, `font-family`, `font-size`, `font-weight`, and other properties.

3. **Link Styles**:
   Customize the appearance of the table of contents links by modifying the `.table-of-contents__link` selector. You can change the `color`, `font-family`, `font-size`, and other properties.

4. **Hover and Active States**:
   Adjust the styles for hover and active states by editing the `.table-of-contents__link:hover`, `.table-of-contents__link--active`, and related selectors. You can change colors, add underlines, or apply other effects.

5. **Visual Indicators for Active Links**:
   Uncomment and modify the `.table-of-contents__link--active::before` selector to add a visual indicator (like a border) for the currently active link.

6. **Backdrop Filters**:
   If you want to apply backdrop filters to create a frosted glass effect, uncomment and customize the `[data-theme="light"] .table-of-contents` and `[data-theme="dark"] .table-of-contents` selectors. Adjust the `backdrop-filter`, `background-color`, and other properties as needed.

Remember to test your changes in both light and dark themes to ensure consistency and readability across different color schemes.

# sidebar.scss

## Overview

The `sidebar.scss` file is a crucial component of the Docusaurus template's styling system. It primarily focuses on customizing the appearance and behavior of the sidebar, navigation menu, and related elements. This file uses SCSS (Sassy CSS) to define styles for various classes and elements, ensuring a consistent and visually appealing sidebar across the documentation site.

Key features of this file include:

1. Styling for active menu links
2. Custom font settings for menu items
3. Dark theme adaptations
4. Customization of dropdown carets
5. Removal of default borders
6. Mobile-specific adjustments
7. Breadcrumb styling

## How can I customize this for my usecase

To customize the `sidebar.scss` file for your specific needs, you can make the following adjustments:

1. **Colors**: Replace color values (e.g., `#313032`, `#A2A1A5`, `#0D0D0D`) with your preferred color scheme. You can also modify the `$color-1` variable in the `design-preferences.scss` file to change the primary color used throughout the sidebar.

2. **Fonts**: Adjust the font family, size, weight, and other properties to match your desired typography. For example:
   ```scss
   .menu__link {
     font-family: YourPreferredFont, sans-serif;
     font-size: 16px;
     font-weight: 400;
   }
   ```

3. **Active link styles**: Modify the appearance of active menu items by changing the `menu__link--active` class properties. You can adjust the background, color, and border-radius to suit your design.

4. **Dark theme**: Customize the dark theme colors by modifying the styles under the `[data-theme="dark"]` selectors.

5. **Dropdown carets**: Replace the SVG content in the `background` property of `.menu__link--sublist-caret:after, .menu__caret:before` to change the dropdown icon.

6. **Breadcrumbs**: Adjust the breadcrumb styles, including colors, font weights, and visibility of specific items.

7. **Mobile menu**: Customize the mobile menu appearance by modifying the styles for `.navbar-sidebar__back` and `.navbar-toggle`.

8. **Scrollbar**: If you want to display the scrollbar for the table of contents, remove or modify the `.theme-doc-toc-desktop::-webkit-scrollbar-track` rule.

Remember to test your changes across different screen sizes and both light and dark themes to ensure a consistent user experience. If you need to make more extensive changes, consider creating additional SCSS files and importing them into your main stylesheet.

# shadcn.scss

## Overview

The `shadcn.scss` file is a crucial component of the Docusaurus template, combining Tailwind CSS utility classes with custom CSS variables for theming. It defines the color scheme and styling for both light and dark modes, ensuring a consistent and customizable appearance across the documentation site.

Key features of this file include:

1. Tailwind CSS directives
2. CSS custom properties (variables) for theming
3. Dark mode support
4. Base styles for HTML elements
5. Custom styles for Markdown content and Docusaurus-specific elements

## How can I customize this for my usecase

To customize the `shadcn.scss` file for your specific needs, you can follow these steps:

1. **Adjust color scheme**: Modify the CSS custom properties in the `:root` and `.dark` selectors to change the color palette for light and dark modes. For example:

   ```scss
   :root {
     --primary: 210 50% 20%; // Change primary color
     --accent: 150 60% 50%; // Change accent color
   }
   ```

2. **Customize typography**: Add or modify typography-related CSS variables to change font styles, sizes, or weights.

3. **Modify component styles**: Adjust the existing styles or add new ones for specific components or elements. For instance:

   ```scss
   .markdown {
     h1 {
       @apply text-3xl font-bold mb-4;
     }
   }
   ```

4. **Add custom classes**: Create new utility classes or component styles to use throughout your documentation:

   ```scss
   .custom-button {
     @apply bg-primary text-white px-4 py-2 rounded-md;
   }
   ```

5. **Override Docusaurus defaults**: If you need to change specific Docusaurus styling, target the appropriate selectors and apply your custom styles:

   ```scss
   #__docusaurus_skipToContent_fallback {
     // Your custom styles here
   }
   ```

6. **Extend Tailwind configuration**: If you need additional Tailwind utilities, you can extend the Tailwind configuration in your `tailwind.config.js` file and use the new classes in this SCSS file.

Remember to test your changes in both light and dark modes to ensure consistency across your documentation site. After making changes, rebuild your Docusaurus site to see the updates take effect.

# secondaryColors.scss

## Overview

The `secondaryColors.scss` file is a SASS stylesheet that defines a set of secondary color variables for use in your Docusaurus template. It provides a comprehensive color palette with various shades and tints for four main colors:

1. A pink/magenta color (color-2)
2. A blue color (color-3)
3. A brown/terra cotta color (color-4)
4. Another blue color (color-5, identical to color-3)

Each main color has 12 variations, ranging from lighter tints to darker shades. These are numbered from 1 (lightest) to 12 (darkest), with the main color typically being the 5th or 6th variation.

## How can I customize this for my usecase

To customize the `secondaryColors.scss` file for your specific needs:

1. **Modify existing colors**: You can adjust the RGB values of the main colors (color-2, color-3, color-4, color-5) to match your brand or design preferences.

   ```scss
   $color-2: rgba(199, 21, 133, 1); // Change these values
   $color-3: rgba(30, 144, 255, 1);
   $color-4: rgba(160, 79, 49, 1);
   $color-5: rgba(30, 144, 255, 1);
   ```

2. **Adjust color variations**: You can fine-tune the tints and shades for each main color by modifying the hex values of their variations.

   ```scss
   $color-2-1: #fe58b5; // Lightest tint
   $color-2-2: #ef48a7;
   // ...
   $color-2-12: #5d002f; // Darkest shade
   ```

3. **Add new color sets**: If you need additional color palettes, you can add new color sets following the same pattern:

   ```scss
   $color-6: rgba(R, G, B, 1);
   $color-6-1: #hexvalue;
   $color-6-2: #hexvalue;
   // ... and so on
   ```

4. **Remove unused colors**: If you don't need all four color sets, you can remove the unused ones to keep your stylesheet lean.

5. **Rename variables**: You might want to give more meaningful names to the color variables based on their purpose in your design:

   ```scss
   $primary-pink: rgba(199, 21, 133, 1);
   $primary-pink-light: #fe58b5;
   $primary-pink-dark: #5d002f;
   ```

Remember to update any references to these color variables in your other SCSS or CSS files after making changes. This will ensure consistency throughout your Docusaurus template.

# searchbar.scss

## Overview

The `searchbar.scss` file is a crucial component of the Docusaurus template's styling, specifically focusing on the search bar functionality and its responsive design. This SCSS file contains styles that control the appearance and behavior of the search bar across different screen sizes and themes (light and dark mode).

Key features of this file include:

1. Centering and positioning of the search bar
2. Responsive design for various screen sizes (mobile, tablet, desktop)
3. Customization of the search button appearance
4. Theme-specific styling for light and dark modes
5. Z-index management for proper layering of UI elements

## How can I customize this for my usecase

To customize the `searchbar.scss` file for your specific needs, you can make the following adjustments:

1. **Search Bar Positioning**: 
   Modify the `.centerSearchBar` class to change the position and layout of the search bar. Adjust the `top`, `right`, `bottom`, and `left` properties as needed.

   ```scss
   .centerSearchBar {
     // Modify these values to change the position
     top: 10px;
     right: 20px;
     // ...
   }
   ```

2. **Responsive Breakpoints**: 
   Adjust the media query breakpoints to match your desired responsive behavior. Current breakpoints are set at 600px, 967px, and 996px.

   ```scss
   @media (max-width: 768px) {
     // Add your custom styles for tablets
   }
   ```

3. **Search Button Styling**: 
   Customize the appearance of the search button by modifying the `.navbar .aa-DetachedSearchButton` class. You can change the border color, background, and dimensions.

   ```scss
   .navbar .aa-DetachedSearchButton {
     border: 2px solid your-color !important;
     background: your-background-color !important;
     // ...
   }
   ```

4. **Theme-Specific Colors**: 
   Adjust the colors for light and dark themes by modifying the `[data-theme='light']` selectors. You can change text colors, background colors, and other theme-specific properties.

   ```scss
   [data-theme='light'] .navbar-sidebar__back {
     color: your-light-theme-color !important;
   }
   ```

5. **Z-index Adjustments**: 
   If you're having issues with element stacking, you can modify the z-index values to ensure proper layering of UI components.

   ```scss
   .navbar-sidebar {
     z-index: your-desired-value !important;
   }
   ```

6. **Mobile-Specific Styles**: 
   Customize the mobile view by modifying the styles within the smaller screen size media queries (e.g., `@media (max-width: 600px)`).

Remember to test your changes across different screen sizes and both light and dark themes to ensure a consistent user experience. After making modifications, rebuild your Docusaurus project to see the changes take effect.

# root-and-body.scss

## Overview

The `root-and-body.scss` file is a crucial part of the Docusaurus template's styling system. It defines CSS variables and styles that control the overall appearance of the website, including color schemes for both light and dark themes, background gradients, and various layout adjustments.

Key features of this file include:

1. Definition of color variables for primary colors and their variations
2. CSS custom properties for Docusaurus theming
3. Separate styles for light and dark themes
4. Animated background gradients
5. Styling for specific Docusaurus elements and classes
6. Responsive design adjustments

## How can I customize this for my use case

To customize the `root-and-body.scss` file for your specific needs, you can make the following adjustments:

1. **Color Scheme**: 
   - Modify the `$color-1` variable and its variations to change the primary color of your site.
   - Adjust the CSS custom properties in the `:root` and `[data-theme="dark"]` selectors to fine-tune the color palette for both light and dark themes.

   ```scss
   $primary: $color-1;
   // Modify other color variables as needed
   
   :root {
     --ifm-color-primary: #{$color-1};
     // Adjust other custom properties
   }
   ```

2. **Background Gradients**:
   - Customize the radial gradients in the `[data-theme="dark"]` and `[data-theme="light"]` selectors to create unique background effects.
   - Modify the `gradientAnimation` keyframes to change the animation behavior.

   ```scss
   [data-theme="dark"] #__docusaurus::before {
     background: radial-gradient(ellipse 349px 354px at 60% 40%, rgba(#YourColor, var(--ellipis-transparency)) 40%, transparent 90%) no-repeat;
     // Adjust other properties as needed
   }
   ```

3. **Layout Adjustments**:
   - Modify the media queries and their associated styles to adjust the layout for different screen sizes.
   - Customize padding, margins, and other layout properties to fit your design preferences.

   ```scss
   [class^="docRoot"] {
     @media (min-width: 1400px) {
       padding-left: 5em;
       padding-right: 5em;
       padding-top: 2em;
     }
     // Add or modify other styles
   }
   ```

4. **Element-Specific Styling**:
   - Add or modify styles for specific elements or classes to customize their appearance.
   - For example, you can adjust the styling for images within documentation:

   ```scss
   [class^="docRoot"] {
     img {
       margin-top: 1.5em;
       margin-bottom: 1.5em;
       // Add other image-specific styles
     }
   }
   ```

5. **Animation and Effects**:
   - Modify the `backdrop-filter` and `-webkit-backdrop-filter` properties to adjust blur and saturation effects.
   - Customize the `animation` property to change the duration or timing function of gradient animations.

Remember to test your changes thoroughly across different themes and screen sizes to ensure a consistent and appealing design throughout your Docusaurus site.

# prose.scss

## Overview

The `prose.scss` file is a crucial part of the styling for the ProseMirror editor in this Docusaurus template. It defines the appearance and layout of various elements within the editor, including tables, code blocks, images, and more. The file also includes responsive design elements for mobile devices.

Key features of this stylesheet include:

1. Table styling with cell selection and column resizing
2. Code and pre-formatted text appearance
3. Image sizing and responsive behavior
4. Blockquote and horizontal rule styling
5. Column layout for content blocks
6. Draggable item styling
7. Responsive design adjustments for mobile devices

## How can I customize this for my usecase

To customize the `prose.scss` file for your specific needs, you can modify various aspects of the stylesheet:

1. **Table styling**: Adjust the border colors, cell padding, or background colors in the `.ProseMirror table` section.

2. **Typography**: Modify the margins, padding, or font styles for elements like paragraphs, lists, and headings.

3. **Code blocks**: Change the background color, font family, or text color for inline code and code blocks in the `code` and `pre` sections.

4. **Images**: Adjust the `max-width` and `height` properties in the `img` selector to control image sizing.

5. **Blockquotes**: Customize the appearance of blockquotes by modifying the `padding-left` and `border-left` properties.

6. **Column layout**: Adjust the `gap`, `padding`, or `border` properties in the `.ProseMirror .column-block` and `.ProseMirror .column` sections to change the appearance of column layouts.

7. **Draggable items**: Modify the styling of draggable items by adjusting properties in the `.draggable-item` section.

8. **Responsive design**: Customize the mobile layout by modifying the media queries at the bottom of the file. You can adjust breakpoints, change the layout, or modify font sizes for smaller screens.

9. **Custom elements**: Add new selectors and styles for any custom elements or plugins you may add to the ProseMirror editor.

To implement your changes, simply edit the `prose.scss` file and adjust the CSS properties as needed. Remember to rebuild your project after making changes to see the updates in your Docusaurus site.

# prose-table.scss

## Overview

The `prose-table.scss` file is a SCSS stylesheet that defines the styling for tables and other elements within the ProseMirror editor. This file is part of an open-source Docusaurus template and is responsible for the visual appearance of content created using the ProseMirror rich text editor.

Key features of this stylesheet include:

1. Table styling with fixed layout and border collapse
2. Cell styling for both regular and header cells
3. Highlighting for selected cells
4. Column resize handle styling
5. Basic typography adjustments for various elements (paragraphs, lists, code blocks, images, blockquotes, and horizontal rules)

## How can I customize this for my usecase

To customize the `prose-table.scss` file for your specific use case, you can modify various aspects of the styling. Here are some ways you can adapt the styles:

1. **Table appearance:**
   - Adjust the `border` property of `td` and `th` elements to change the border style, color, or width.
   - Modify the `padding` values to increase or decrease cell spacing.
   - Change the `background-color` of `th` elements to use a different color for table headers.

2. **Selected cell highlighting:**
   - Customize the `background` color and opacity of the `.selectedCell:after` pseudo-element to change the appearance of selected cells.

3. **Column resize handle:**
   - Modify the `width`, `background-color`, or `right` position of the `.column-resize-handle` to adjust its appearance or position.

4. **Typography:**
   - Change the `margin-top` value of `> * + *` to adjust the spacing between elements.
   - Modify the `padding` of `ul` and `ol` elements to adjust list indentation.

5. **Code blocks:**
   - Customize the `background-color` and `color` of `pre` elements to change the appearance of code blocks.
   - Adjust the `font-family` to use a different monospace font for code.

6. **Blockquotes:**
   - Modify the `border-left` property of `blockquote` elements to change the style of the left border.

7. **Horizontal rules:**
   - Adjust the `border-top` property of `hr` elements to change the appearance of horizontal rules.

To implement these customizations, open the `prose-table.scss` file and modify the relevant CSS properties. After making your changes, make sure to rebuild your Docusaurus project to apply the updated styles.

Remember to test your changes thoroughly to ensure they don't negatively impact the functionality or appearance of the ProseMirror editor in your Docusaurus template.

# navbar.scss

## Overview

The `navbar.scss` file is a crucial component of the open-source Docusaurus template, responsible for styling the navigation bar. It provides custom styles for both light and dark themes, implements a fixed-top navbar, and includes responsive design elements.

Key features of this file include:

1. Theme-specific styles for light and dark modes
2. Sticky positioning for the navbar
3. Blur effect for the navbar background
4. Custom styling for theme toggle buttons
5. Responsive design adjustments

## How can I customize this for my usecase

To customize the `navbar.scss` file for your specific needs, consider the following approaches:

1. **Adjust color schemes:**
   Modify the background colors and text colors for both light and dark themes to match your brand identity.

   ```scss
   [data-theme="dark"] .navbar--fixed-top {
     background-color: rgb(8 28 69 / 30%);
     color: white;
   }

   [data-theme="light"] .navbar--fixed-top {
     background-color: rgba(255, 255, 255, 0.34);
     color: black;
   }
   ```

2. **Customize navbar height:**
   Change the height of the navbar by modifying the `height` property.

   ```scss
   .navbar--fixed-top {
     height: 4.375rem; // Adjust this value as needed
   }
   ```

3. **Modify blur effect:**
   Adjust the blur intensity and saturation of the navbar background.

   ```scss
   .navbar--fixed-top {
     backdrop-filter: blur(16px) saturate(180%);
     -webkit-backdrop-filter: blur(16px) saturate(180%);
   }
   ```

4. **Update theme toggle buttons:**
   Replace the SVG images for the theme toggle buttons with your own custom icons.

   ```scss
   [data-theme="dark"] .navbar__items--right {
     [class^="toggle"] {
       .clean-btn {
         background-image: url("path/to/your/dark-theme-icon.svg") !important;
       }
     }
   }

   .navbar__items--right {
     [class^="toggle"] {
       .clean-btn {
         background-image: url("path/to/your/light-theme-icon.svg");
       }
     }
   }
   ```

5. **Adjust responsive breakpoints:**
   Modify the media queries to better suit your design needs.

   ```scss
   @media (min-width: 1400px) {
     .navbar {
       padding-left: 2em;
       padding-right: 2em;
     }
   }

   @media (max-width: 767px) {
     .navbar__title {
       display: none !important;
     }
   }
   ```

6. **Customize logo dimensions:**
   Adjust the minimum width and height of the navbar logo.

   ```scss
   .navbar__logo {
     min-width: 1.84588rem;
     min-height: 1.6875rem;
   }
   ```

Remember to test your changes across different screen sizes and themes to ensure a consistent user experience. You may also need to update corresponding HTML and JavaScript files if you make significant changes to the navbar structure or functionality.

# mobilelanding.scss

## Overview

The `mobilelanding.scss` file is a crucial part of the responsive design for the Dev-Docs landing page. It contains styles specifically tailored for mobile devices with a maximum width of 767px. This file adjusts various elements of the landing page to ensure optimal display and functionality on smaller screens.

Key features of this stylesheet include:

1. Responsive layout adjustments for the main content area
2. Mobile-specific styling for headings, buttons, and grid layouts
3. Custom styles for hero sections and integration grids
4. Font size and spacing modifications for better readability on small screens
5. Hiding certain elements that may not be suitable for mobile view

## How can I customize this for my usecase

To customize the `mobilelanding.scss` file for your specific needs, consider the following approaches:

1. **Adjust breakpoints**: The current breakpoint is set to 767px. You can modify this value to target different screen sizes:

   ```scss
   @media (max-width: 767px) {
     // Your styles here
   }
   ```

2. **Customize typography**: Modify font sizes, weights, and styles to match your brand:

   ```scss
   h1 {
     font-size: 2.5rem;
     font-weight: 700;
     font-family: 'Your-Preferred-Font', sans-serif;
   }
   ```

3. **Modify color scheme**: Replace color values with your own brand colors:

   ```scss
   .main-btn {
     border: 2px solid #your-color;
     background: #your-background-color;
   }
   ```

4. **Adjust layout and spacing**: Modify padding, margins, and flex properties to fit your design:

   ```scss
   .dev-docs-landing {
     min-height: 320ch;
     display: flex;
     justify-content: flex-start;
     align-items: flex-start;
   }
   ```

5. **Customize hero sections**: Modify background images, colors, and content layout for each hero section:

   ```scss
   .second-hero {
     background-image: url("/path/to/your/image.png");
     background-position: top left;
     background-repeat: no-repeat;
   }
   ```

6. **Adjust or remove specific components**: You can modify or remove styles for components that don't fit your needs, such as the integration grid or draggable elements.

Remember to test your changes across various mobile devices and screen sizes to ensure a consistent user experience. You may also want to use CSS variables for colors and sizes to make global changes easier to manage.

# legacy.scss

## Overview

The `legacy.scss` file is a crucial component of the open-source Docusaurus template. It contains various SCSS styles that define the appearance and behavior of different elements in the template. This file includes styles for cards, buttons, tables, and responsive design elements.

Key features of this file include:

1. Styling for different types of cards (e.g., magic cards, gradient hover cards)
2. Button styles with gradient effects
3. Table styling
4. Responsive design adjustments
5. Custom animations
6. Utility classes for extending width and height

## How can I customize this for my usecase

To customize the `legacy.scss` file for your specific use case, you can follow these steps:

1. **Color Scheme**: Modify the color variables (e.g., `$color-1`, `$color-2`, etc.) to match your brand's color scheme.

   ```scss
   $color-1: #your-color-here;
   $color-2: #your-color-here;
   // ... and so on
   ```

2. **Card Styles**: Adjust the card styles by modifying classes like `.magic-card`, `.gradient-hover-card-one`, etc. You can change properties such as `border-radius`, `padding`, or `box-shadow`.

   ```scss
   .gradient-hover-card-one {
     border-radius: 20px; // Change the border radius
     padding: 40px 20px; // Adjust padding
     // Add or modify other properties
   }
   ```

3. **Button Styles**: Customize button appearances by modifying classes like `.button`, `.border-button`, or `.gradient-button`.

   ```scss
   .gradient-button {
     background-image: linear-gradient(to right, #your-color-1, #your-color-2);
     // Modify other properties as needed
   }
   ```

4. **Responsive Design**: Adjust the media queries to fit your specific breakpoints and modify the styles for different screen sizes.

   ```scss
   @media (max-width: 768px) {
     // Your custom styles for mobile devices
   }

   @media (max-width: 1024px) {
     // Your custom styles for tablets
   }
   ```

5. **Custom Animations**: Modify existing animations or add new ones to suit your needs.

   ```scss
   @keyframes your-custom-animation {
     0% { /* start state */ }
     100% { /* end state */ }
   }
   ```

6. **Typography**: Adjust font sizes, line heights, and letter spacing to match your design preferences.

   ```scss
   .your-text-class {
     font-size: 16px;
     line-height: 1.5;
     letter-spacing: 0.5px;
   }
   ```

7. **Utility Classes**: Add or modify utility classes to extend functionality.

   ```scss
   .your-custom-utility-class {
     // Your custom styles
   }
   ```

Remember to test your changes thoroughly across different devices and browsers to ensure compatibility and responsiveness. If you're not familiar with SCSS, consider learning its basics to take full advantage of its features like variables, mixins, and nesting.

# landingpage.scss

## Overview

The `landingpage.scss` file is a crucial component of the styling for the landing page in this Docusaurus template. It contains a variety of CSS styles that define the look and feel of the landing page, including layout, typography, color schemes, and responsive design elements.

Key features of this stylesheet include:

1. Responsive design for various screen sizes
2. Custom styling for headings, paragraphs, and other text elements
3. Glassmorphism effects for certain UI components
4. Dark and light theme support
5. Custom styles for draggable items and grid layouts
6. Specific styling for hero sections and contact forms

## How can I customize this for my usecase

To customize the `landingpage.scss` file for your specific needs, you can follow these steps:

1. **Color Scheme**: Modify the color variables to match your brand's color palette. Look for color definitions like `#cecef8`, `#a4fad1`, etc., and replace them with your preferred colors.

2. **Typography**: Adjust font sizes, weights, and families to align with your design preferences. For example:
   ```scss
   h1 {
     font-size: 4.88313rem;
     font-family: YourPreferredFont, sans-serif;
     font-weight: 700;
   }
   ```

3. **Layout**: Modify the layout properties such as padding, margins, and grid settings to fit your content structure. For instance:
   ```scss
   .content {
     padding-left: 5em;
     padding-right: 5em;
     max-width: 90%;
   }
   ```

4. **Responsive Design**: Adjust the media queries to ensure your landing page looks great on all devices. You can modify existing breakpoints or add new ones:
   ```scss
   @media (max-width: 992px) {
     // Your custom styles for tablets
   }
   ```

5. **Custom Components**: Add or modify styles for specific components you've created. For example:
   ```scss
   .my-custom-component {
     background-color: #f0f0f0;
     border-radius: 8px;
     padding: 1rem;
   }
   ```

6. **Theme Customization**: Modify the dark and light theme styles to match your preferences:
   ```scss
   [data-theme="dark"] {
     // Your custom dark theme styles
   }

   [data-theme="light"] {
     // Your custom light theme styles
   }
   ```

7. **Effects and Animations**: Customize or add new effects like the glassmorphism style:
   ```scss
   .glass-effect {
     backdrop-filter: blur(10px);
     background-color: rgba(255, 255, 255, 0.1);
   }
   ```

Remember to test your changes across different browsers and devices to ensure compatibility and responsiveness. You may also want to use CSS preprocessor features like variables and mixins to make your customizations more maintainable.

# headings-and-paragraphs.scss

## Overview

This SCSS file defines styling for headings, paragraphs, and other text elements in a Docusaurus template. It includes styles for both light and dark themes, as well as responsive typography and consistent spacing.

Key features:
- Theme-specific styles for light and dark modes
- Consistent typography for headings (h1-h6) and paragraphs
- Responsive font sizes and weights
- Uniform spacing using a base margin and vertical margin mixin
- Styles for lists, images, and links

## How can I customize this for my usecase

1. **Modify theme colors:**
   - Adjust the color values in the `[data-theme="dark"]` and `[data-theme="light"]` sections to match your brand colors.

2. **Change font families:**
   - Replace the `font-family` declarations with your preferred fonts. You can use system fonts, web fonts, or custom fonts.

3. **Adjust typography:**
   - Modify the `font-size`, `font-weight`, `line-height`, and `letter-spacing` properties for headings and paragraphs to match your design requirements.

4. **Customize spacing:**
   - Change the `$base-margin` value to increase or decrease the overall spacing between elements.
   - Adjust the multipliers in the `vertical-margin` mixin calls to fine-tune spacing for specific heading levels.

5. **Modify link styles:**
   - Update the `a` and `a:hover` selectors to change link colors and hover effects.

6. **Add custom classes:**
   - Create new class selectors for specific elements or components in your documentation.

7. **Responsive design:**
   - Add media queries to adjust styles for different screen sizes.

8. **Extend existing styles:**
   - Use SCSS nesting and extend features to add more specific styles while maintaining the base design.

Example customization:

```scss
// Custom color variable
$brand-primary: #3498db;

[data-theme="light"] {
  h1, h2, h3, h4, h5, h6 {
    color: $brand-primary !important;
  }
}

// Custom heading style
h1 {
  font-size: 36px;
  text-transform: uppercase;
}

// Responsive font size
@media (max-width: 768px) {
  h1 {
    font-size: 28px;
  }
}
```

Remember to test your changes across different themes and screen sizes to ensure consistency and readability throughout your documentation.

# footer.scss

## Overview

The `footer.scss` file is a crucial component of the Docusaurus template, responsible for styling the footer section of the website. It contains SCSS code that defines the appearance and layout of various footer elements, including social media icons, pagination navigation, and copyright information.

Key features of this stylesheet include:

1. Theme-specific styling for dark and light modes
2. Custom styling for pagination navigation links
3. Social media icon implementations (GitHub, Instagram, Discord, LinkedIn)
4. Footer layout and alignment adjustments
5. Responsive design considerations

## How can I customize this for my usecase

To customize the footer styles for your specific needs, you can modify the `footer.scss` file in the following ways:

1. **Adjust theme-specific styles:**
   Modify the styles within `[data-theme="dark"]` and `[data-theme="light"]` selectors to change the appearance of the footer in different color modes.

   ```scss
   [data-theme="dark"] .footer--dark {
     // Your custom dark mode styles
   }

   [data-theme="light"] .footer--dark {
     // Your custom light mode styles
   }
   ```

2. **Customize pagination navigation:**
   Modify the `.pagination-nav__link` and related classes to change the appearance of the "Previous" and "Next" navigation buttons.

   ```scss
   .pagination-nav__link {
     // Your custom styles for navigation links
   }
   ```

3. **Update social media icons:**
   Add or remove social media icons by modifying the respective classes (e.g., `.github`, `.instagram`, `.discord`, `.linkedin`). You can also change the icon sizes or add new icons:

   ```scss
   .new-social-icon {
     width: 24px;
     height: 24px;
     background-image: url("/path/to/your/icon.svg");
     // Other necessary styles
   }
   ```

4. **Adjust footer layout:**
   Modify the `.footer`, `.container-fluid`, and `.row.footer__links` classes to change the overall layout and spacing of the footer elements:

   ```scss
   .footer {
     // Your custom footer styles
   }

   .container-fluid {
     // Adjust max-width or other properties
   }

   .row.footer__links {
     // Modify the layout of footer links
   }
   ```

5. **Customize typography:**
   Update font styles for various footer elements, such as the copyright text:

   ```scss
   .footer__copyright {
     font-family: YourPreferredFont, sans-serif;
     font-size: 12px;
     // Other typography styles
   }
   ```

6. **Add responsive styles:**
   Implement media queries to ensure the footer looks good on different screen sizes:

   ```scss
   @media (max-width: 768px) {
     .footer {
       // Styles for smaller screens
     }
   }
   ```

Remember to test your changes across different browsers and devices to ensure consistency and proper functionality. If you're using CSS modules or a different styling approach in your Docusaurus setup, you may need to adjust the selectors or import statements accordingly.

# design-preferences.scss

## Overview

The `design-preferences.scss` file is a crucial component of the open-source Docusaurus template's styling system. It defines a comprehensive color palette using SCSS variables, allowing for easy customization and consistent theming across the project.

This file contains five main color sets (color-1 to color-5), each with a base color and 12 variations. These color sets provide a wide range of shades that can be used throughout the template for various UI elements, ensuring a cohesive and visually appealing design.

## How can I customize this for my usecase

To customize the `design-preferences.scss` file for your specific use case, follow these steps:

1. **Modify base colors**: 
   - Locate the base color variables (e.g., `$color-1`, `$color-2`, etc.).
   - Replace the hexadecimal or rgba values with your desired colors.

2. **Adjust color variations**:
   - For each base color, there are 12 variations (e.g., `$color-1-1` to `$color-1-12`).
   - You can modify these variations to create your own custom color palette.
   - Ensure a good contrast ratio between variations for accessibility.

3. **Add new color sets**:
   - If needed, you can add new color sets by following the existing pattern.
   - For example, you could add `$color-6` and its variations.

4. **Use variables in your styles**:
   - In your other SCSS or CSS files, use these color variables to maintain consistency.
   - For example: `background-color: $color-1-3;`

5. **Consider creating theme variations**:
   - You could create multiple versions of this file for different themes (e.g., light and dark modes).

6. **Document your changes**:
   - Add comments to explain the purpose of each color or any specific usage guidelines.

7. **Test your changes**:
   - After modifying the colors, thoroughly test your site to ensure all elements look as intended with the new color scheme.

By customizing this file, you can easily adapt the template's color scheme to match your brand or design preferences, ensuring a unique and cohesive look for your Docusaurus site.

# custom.scss

## Overview

The `custom.scss` file is a central stylesheet for a Docusaurus-based project. It imports various SCSS modules and Tailwind CSS utilities to provide a comprehensive styling foundation for the entire site. This file acts as the main entry point for all custom styles and design preferences.

Key components imported in this file include:

1. Tailwind CSS base, components, and utilities
2. Custom design preferences and secondary colors
3. Component-specific styles (e.g., sidebar, navbar, footer)
4. Typography styles for headings, paragraphs, and prose
5. Styles for specific features like the searchbar, table of contents, and chatbot
6. Styles for different page types (e.g., landing page, blog, cards)

## How can I customize this for my usecase

To customize the `custom.scss` file for your specific needs:

1. **Tailwind CSS customization**: 
   - Modify the Tailwind configuration file to change default styles, add new utility classes, or extend existing ones.

2. **Design preferences**: 
   - Edit the `design-preferences.scss` and `secondaryColors.scss` files to adjust color schemes, fonts, and other global design elements.

3. **Component-specific styles**: 
   - Modify or create new SCSS files for individual components (e.g., `sidebar.scss`, `navbar.scss`) to customize their appearance.

4. **Typography**: 
   - Adjust `headings-and-paragraphs.scss` and `prose.scss` to fine-tune text styles across your site.

5. **Feature-specific styles**: 
   - Customize styles for specific features by modifying files like `searchbar.scss`, `table-of-contents.scss`, or `chatbot.scss`.

6. **Page-type styles**: 
   - Tailor the appearance of different page types by editing files such as `landingpage.scss`, `blog.scss`, or `cards.scss`.

7. **Add new imports**: 
   - Create and import new SCSS modules for additional custom styles or components specific to your project.

8. **Remove unused imports**: 
   - If certain features or components are not used in your project, you can remove their corresponding import statements to reduce the file size.

9. **Order of imports**: 
   - Adjust the order of imports if you need to override specific styles or ensure proper cascading of CSS rules.

Remember to rebuild your project after making changes to see the effects of your customizations.

# custom.css

## Overview

This file, `custom.css`, is a crucial part of the Docusaurus template's styling system. It imports the core Tailwind CSS modules, which provide a utility-first CSS framework. This approach allows for rapid UI development with pre-defined classes.

The file consists of three main imports:

1. `@import 'tailwindcss/base';`
2. `@import 'tailwindcss/components';`
3. `@import 'tailwindcss/utilities';`

These imports bring in the base styles, component styles, and utility classes from Tailwind CSS, respectively.

## How can I customize this for my usecase

To customize the `custom.css` file for your specific needs, you can:

1. **Add custom CSS rules**: You can add your own CSS rules below the Tailwind imports. These will override or complement the Tailwind styles.

   ```css
   @import 'tailwindcss/base';
   @import 'tailwindcss/components';
   @import 'tailwindcss/utilities';

   /* Your custom CSS here */
   .my-custom-class {
     color: #ff0000;
   }
   ```

2. **Extend Tailwind's configuration**: In your `tailwind.config.js` file, you can extend or override Tailwind's default theme, add new utility classes, or configure plugins.

   ```js
   module.exports = {
     theme: {
       extend: {
         colors: {
           'custom-blue': '#1da1f2',
         },
       },
     },
     // ... other configurations
   };
   ```

3. **Use Tailwind's @apply directive**: You can use Tailwind's utility classes within your custom CSS using the `@apply` directive.

   ```css
   .btn-primary {
     @apply py-2 px-4 bg-blue-500 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75;
   }
   ```

4. **Import additional CSS files**: If you have other CSS files for specific components or pages, you can import them in this file.

   ```css
   @import 'tailwindcss/base';
   @import 'tailwindcss/components';
   @import 'tailwindcss/utilities';

   @import './my-component-styles.css';
   @import './my-page-styles.css';
   ```

Remember to rebuild your project after making changes to see the effects of your customizations.

# custom-templates.scss

## Overview

The `custom-templates.scss` file is part of an open-source Docusaurus template. It contains custom SCSS styles that define various visual elements and layouts used throughout the template. These styles are designed to enhance the appearance and functionality of the template, providing a range of customizable components such as cards, grids, and responsive designs.

Key features of this stylesheet include:

1. Responsive grid layouts
2. Custom card designs with hover effects
3. Glassmorphism effects
4. Gradient animations
5. Media queries for different screen sizes
6. Syntax highlighting for code blocks
7. Custom table styles

## How can I customize this for my use case

To customize the `custom-templates.scss` file for your specific needs, you can follow these steps:

1. **Color Scheme**: 
   - Look for color variables (e.g., `$color-1`, `$color-2`, etc.) and modify them to match your desired color scheme.
   - Update gradient colors in various classes like `.gradient-hover-card-one`, `.gradient-hover-card-two`, etc.

2. **Card Styles**:
   - Modify classes like `.general-card`, `.glass-card-one`, `.gradient-hover-card-one`, etc., to change the appearance of different card types.
   - Adjust padding, border-radius, and box-shadow properties to alter the card design.

3. **Grid Layouts**:
   - Customize the `.draggable-grid` and `.draggable-logo-grid` classes to change the layout of grid elements.
   - Modify `flex` properties and `gap` values to adjust spacing and sizing.

4. **Responsive Design**:
   - Edit the media queries (`@media (max-width: 768px)` and `@media (max-width: 1024px)`) to adjust the responsive behavior for different screen sizes.
   - Modify properties like `flex`, `height`, and `padding` within these media queries to fine-tune the mobile and tablet layouts.

5. **Typography**:
   - Adjust font sizes, line heights, and letter spacing in various classes to match your typography preferences.

6. **Animations**:
   - Modify the `@keyframes rotation` and `@keyframes rotate` rules to change animation behaviors.
   - Adjust animation properties in classes like `.gradient-hover-card-one:hover::before` to alter hover effects.

7. **Code Highlighting**:
   - Customize the colors in the `.ProseMirror pre` section to change the appearance of syntax highlighting in code blocks.

8. **Custom Components**:
   - Add new classes or modify existing ones like `.callout`, `.background-landing`, or `.radial-card-content` to create or adjust custom components.

Remember to test your changes thoroughly across different devices and browsers to ensure compatibility and desired appearance. You may also want to use CSS preprocessing tools to take full advantage of SCSS features like variables and mixins for more efficient customization.

# coding-languages.scss

## Overview

The `coding-languages.scss` file is a Sass (SCSS) stylesheet that contains styling rules for specific language-related elements in a Docusaurus template. This file focuses on the appearance of Markdown language elements within the documentation.

The file currently contains a single rule set for the `.language-markdown` class, which is likely used to style code blocks or inline code snippets that contain Markdown syntax.

## How can I customize this for my use case

To customize the `coding-languages.scss` file for your specific needs, you can modify the existing rules or add new ones. Here are some ways you can adapt this file:

1. Adjust the `.language-markdown` class:
   - Change the `opacity` value to make Markdown syntax more or less visible.
   - Modify the `height` and `width` properties to alter the size of Markdown code blocks.
   - Adjust the `overflow` property to change how content behaves when it exceeds the container's dimensions.

2. Add styles for other language classes:
   - Create new rule sets for other language-specific classes, such as `.language-javascript`, `.language-python`, etc.
   - Example:
     ```scss
     .language-javascript {
       background-color: #f7df1e;
       color: #000000;
     }
     ```

3. Implement syntax highlighting:
   - Add rules to highlight different parts of the code syntax, such as keywords, strings, or comments.
   - Example:
     ```scss
     .language-markdown {
       .keyword {
         color: #0000ff;
       }
       .string {
         color: #008000;
       }
     }
     ```

4. Create a common style for all code blocks:
   - Use a more general selector to apply styles to all language classes.
   - Example:
     ```scss
     [class^="language-"] {
       font-family: 'Courier New', Courier, monospace;
       border-radius: 4px;
       padding: 1em;
     }
     ```

5. Add responsive designs:
   - Use media queries to adjust the appearance of code blocks on different screen sizes.
   - Example:
     ```scss
     @media (max-width: 768px) {
       .language-markdown {
         width: 100%;
         height: auto;
       }
     }
     ```

Remember to test your changes thoroughly to ensure they work well with your Docusaurus template and provide a good user experience across different devices and browsers.

# chatbot.scss

## Overview

The `chatbot.scss` file contains styling for a chat interface, likely used in a Docusaurus-based website. This file defines the appearance and layout of various chat components, including the chat box, messages, input fields, and toggle buttons. It also includes responsive design adjustments for different screen sizes and supports both light and dark themes.

Key features of this stylesheet include:

- Styling for a fixed-position chat box
- Message bubble designs for user and bot messages
- Loading animation for pending messages
- Responsive design for mobile and tablet devices
- Theme-specific styles for light and dark modes
- Fullscreen chat mode
- Styling for code blocks within chat messages

## How can I customize this for my usecase

To customize the chat interface for your specific needs, you can modify various aspects of the `chatbot.scss` file:

1. **Colors and Theme:**
   - Adjust the color scheme by modifying color values throughout the file.
   - Customize the `[data-theme="dark"]` and `[data-theme="light"]` selectors to fine-tune the appearance for different themes.

2. **Layout and Positioning:**
   - Change the `position`, `bottom`, `right`, `width`, and `height` properties of the `.chat-box` class to adjust the chat box's size and position.
   - Modify the `border-radius` values to change the roundness of various elements.

3. **Typography:**
   - Update `font-family`, `font-size`, `font-weight`, and other text-related properties to match your preferred typography.

4. **Responsive Design:**
   - Adjust the media queries at the bottom of the file to fine-tune the layout for different screen sizes.

5. **Chat Messages:**
   - Customize the `.user-message` and `.bot-message` classes to change the appearance of chat bubbles.
   - Modify the `.loading-dots` animation for a different loading indicator.

6. **Input and Buttons:**
   - Update the `.chat-box__input` and `.chat-box__button` classes to style the input field and send button.

7. **Special Features:**
   - Customize the `.full-screen` class to change how the chat box appears in fullscreen mode.
   - Modify the `.copy-button` class to adjust the appearance of the code copy button.

8. **Animations:**
   - Adjust the `transition` properties and `@keyframes` definitions to change animations and transitions.

Remember to test your changes across different devices and themes to ensure a consistent user experience. You may also want to consider adding new classes or modifying existing ones to introduce additional features or styling options specific to your project's needs.

# cards.scss

## Overview

The `cards.scss` file is part of an open-source Docusaurus template. It contains SCSS styles that implement a glassmorphism effect for cards, specifically for the dark theme. This effect creates a semi-transparent, frosted glass appearance that can enhance the visual appeal of card components in your Docusaurus site.

The file uses the `[data-theme="dark"]` selector to apply these styles only when the dark theme is active. The glassmorphism effect is achieved through a combination of backdrop filters, background colors, and border properties.

## How can I customize this for my usecase

To customize the glassmorphism card effect for your specific use case, you can modify the following properties within the `.card` class:

1. **Blur and saturation**: Adjust the `backdrop-filter` and `-webkit-backdrop-filter` values to change the blur intensity and saturation. For example:

   ```scss
   backdrop-filter: blur(10px) saturate(180%);
   -webkit-backdrop-filter: blur(10px) saturate(180%);
   ```

2. **Background color**: Modify the `background-color` to change the card's base color and opacity:

   ```scss
   background-color: rgba(17, 25, 40, 0.75);
   ```

3. **Border radius**: Adjust the `border-radius` to change the card's corner roundness:

   ```scss
   border-radius: 16px;
   ```

4. **Border color and opacity**: Modify the `border` property to change the card's border appearance:

   ```scss
   border: 1px solid rgba(255, 255, 255, 0.2);
   ```

5. **Light theme support**: To add glassmorphism effects for the light theme, you can create a new selector outside the `[data-theme="dark"]` block:

   ```scss
   [data-theme="light"] {
     .card {
       // Light theme glassmorphism styles
     }
   }
   ```

Remember to test your changes in different browsers, as some may not fully support backdrop filters. You may need to provide fallback styles for better cross-browser compatibility.

# blog.scss

## Overview

The `blog.scss` file is a crucial part of the Docusaurus template's styling system, specifically tailored for the blog section. It contains SCSS (Sassy CSS) code that defines the layout, appearance, and responsive behavior of various blog-related components.

Key features of this file include:

1. Responsive design adjustments for different screen sizes
2. Custom styling for blog post headers and content
3. Layout modifications for both blog list and individual post pages
4. Conditional styling based on theme (light/dark mode)
5. Customizations for typography, spacing, and element visibility

## How can I customize this for my usecase

To customize the `blog.scss` file for your specific needs, consider the following approaches:

1. **Modify existing styles:**
   - Adjust color schemes, fonts, or spacing by changing values in the existing CSS rules.
   - Example: To change the font size of blog post content, locate the `.dev-docs-blog p` selector and modify the `font-size` property.

2. **Add new style rules:**
   - Create new CSS selectors to target specific elements in your blog layout.
   - Example: To add a custom background to your blog sidebar, you could add:
     ```scss
     .blog-sidebar {
       background-color: #f0f0f0;
       padding: 1rem;
     }
     ```

3. **Responsive design adjustments:**
   - Modify or add media queries to fine-tune the layout for different screen sizes.
   - Example: To adjust the blog header title for medium-sized screens, you could add:
     ```scss
     @media (min-width: 768px) and (max-width: 1023px) {
       .blog-header-title-card h1 {
         font-size: 48px;
       }
     }
     ```

4. **Conditional styling:**
   - Utilize the existing `conditional-styles` mixin or create your own to apply styles based on specific conditions.
   - Example: To hide a certain element only on the blog list page, you could add:
     ```scss
     .blog-list-page {
       @include conditional-styles("some-class") {
         .element-to-hide {
           display: none;
         }
       }
     }
     ```

5. **Theme customization:**
   - Modify or add styles for dark mode by using the `[data-theme="dark"]` selector.
   - Example: To change link colors in dark mode, you could add:
     ```scss
     [data-theme="dark"] {
       .blog-content a {
         color: #00ffff;
       }
     }
     ```

Remember to test your changes thoroughly across different devices and browsers to ensure a consistent experience for all users. You may also need to rebuild your Docusaurus site to see the changes take effect.