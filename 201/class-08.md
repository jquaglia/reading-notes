# Class 8

## Layout

### Key Conecepts in Positioning Elements

Building Blocks.

- CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.

Containing Elements

- If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

### Controlling the position of elements

CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property. To indicate where a box should be positioned, you may also need to use box offset properties to tell the browser how far from the top or bottom and left or right it should be placed.

- `position: static`

- `position: relative`

- `position: absolute`

- `position: fixed`

### Overlapping elements

- `z-index` When you use relative or fixed or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page.

### Screen Sizes

- Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.

### Screen Resolution

- Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.

### Page Sizes

- Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens)

### Fixed width layouts

- Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.

### Liquid Layouts

- Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.

### Layout Grids

- Composition in any visual art is the placement or arrangement of visual elements - how they are organzied on a page. Many designers use a grid structure to help them position items on a page, and the same is true for web designers.

### CSS Frameworks

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.

### Summary

- `<div>` elements are often used as containing elements to group together sections of a page.

- Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.

- The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width)

- Pages can be fixed width or liquid layouts.

- Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels.

- Grids help create professional and flexible designs.

- CSS Frameworks provide rules for common tasks.

- You can include multiple CSS file in one page.

[back to README](../README.md)
