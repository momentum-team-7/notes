# Responsive Layout

Front-end developers need to think about the size of the screen that will display a page.

Responsive design means creating a layout that can adapt to the size of the window that is displaying it.

---

## The viewport meta tag

You need this tag in the `head` section of your page to allow the page to resize.

```html
<meta name="viewport" content="width=device-width, initial-scale=1" />
```

### [MDN viewport meta tag](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)

---

## Techniques to create responsive layouts

1. A flexible, grid-based page structure
2. Flexible images
3. Media queries

---

## The Grid

Designers rely on the intrinsic order of columns and rows to give meaning and shape to page structure.

A grid structure guides the arrangement and spacing of the boxes on the page.

[Material Design example of a responsive grid](https://material.io/design/layout/responsive-layout-grid.html)

---

## Making a flexible grid

- Use percentage measurements for elements inside your container
- Include margins
- Grids don't have to be a certain number of columns or even columns of equal size
- For your grid container, consider px or rem for width and % for max-width

---

## Flexible images

```css
img {
  max-width: 100%;
  height: auto;
}
```

The max-width property ensures that the image width will not exceed the size of its container.

The height property will maintain the image's aspect ratio.

---

## Media Queries

```css
@media screen and (max-width: 1024px) {...}
@media screen and (min-width: 768px) and (max-width: 1023px) {...}
@media print {...} /* if the page is printed by the user */
@media (max-width: 576px) {...} /* applies to all types */
```

Media types to keep in mind are print and screen. Including a media type in a media query is optional.

---

## Breakpoints

Device sizes are going to change all the time, so don't worry about getting the perfect ones. Use whatever makes sense to you.

People do like standards, so here are some, taken from Bootstrap 4.

- **phones**: >= 576px
- **tablets**: >= 768px
- **desktops**: >= 992px
- **big desktops**: >= 1200px

[Bootstrap 4 responsive breakpoints](https://getbootstrap.com/docs/4.0/layout/overview/#responsive-breakpoints)

---

## Basic Web Design principles for developers

- typography and whitespace
- principle of least surprise
- aim for clean and simple
- judicious use of color
  - start only with black and white; add color last and with purpose
  - rely on neutrals then choose a base color and an accent color

### [7 Rules for Creating Gorgeous UIs](https://medium.com/@erikdkennedy/7-rules-for-creating-gorgeous-ui-part-1-559d4e805cda)
