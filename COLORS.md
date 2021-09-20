# Primary Color / Styles for GWF Platform

## Fade Colors

- Light BG Color: #c5eec5
- Dark BG Color: #43a047

Font Family: Comfortaa, Roboto, "Helvetica Neue", Arial, sans-serif
Standard letter Spacing: 0.25px

> Header (Background fade) from Project Page

```css
.head-area .head-content {
    height: 100vh;
    color: #ffffff;
    z-index: 6;
    padding-top: 5.125rem;
    background: -webkit-gradient(
    linear,
    left top,
    right top,
    from(#c5eec5),
    to(#43a047)
  );
    background: -webkit-linear-gradient(left, #c5eec5, #43a047);
    background: -moz-linear-gradient(left, #c5eec5, #43a047);
    background: -o-linear-gradient(left, #c5eec5, #43a047);
    background: linear-gradient(to right, #c5eec5, #43a047);
}
```
