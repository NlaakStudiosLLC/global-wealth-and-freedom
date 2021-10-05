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

## Loading Page

```html
<div id="loader-wrapper">
      <svg viewBox=" 0 0 512 512" id="loader">
        <linearGradient id="loaderLinearColors" x1="0" y1="0" x2="1" y2="1">
          <stop offset="5%" stop-color="#28bcfd"></stop>
          <stop offset="100%" stop-color="#1d78ff"></stop>
        </linearGradient>
        <g>
          <circle cx="256" cy="256" r="150" fill="none" stroke="url(#loaderLinearColors)"></circle>
        </g>
        <g>
          <circle cx="256" cy="256" r="125" fill="none" stroke="url(#loaderLinearColors)"></circle>
        </g>
        <g>
          <circle cx="256" cy="256" r="100" fill="none" stroke="url(#loaderLinearColors)"></circle>
        </g>
        <g>
          <circle cx="256" cy="256" r="75" fill="none" stroke="url(#loaderLinearColors)"></circle>
        </g>
        <circle cx="256" cy="256" r="60" fill="url(#loaderImage)" stroke="none" stroke-width="0"></circle>

        <!-- Change the preloader logo here -->
        <defs>
          <pattern id="loaderImage" height="100%" width="100%" patternContentUnits="objectBoundingBox">
            <image href="theme-assets/images/gwf_logo_1024.png" preserveAspectRatio="none" width="1" height="1"></image>
          </pattern>
        </defs>
      </svg>

      <div class="loader-section section-left"></div>
      <div class="loader-section section-right"></div>
    </div>
```

```css
.loaded #loader-wrapper {
    visibility: hidden;
    -webkit-transform: translateY(-100%);
    -moz-transform: translateY(-100%);
    -ms-transform: translateY(-100%);
    -o-transform: translateY(-100%);
    transform: translateY(-100%);
    -webkit-transition: all 0.3s 1s ease-out;
    -o-transition: all 0.3s 1s ease-out;
    -moz-transition: all 0.3s 1s ease-out;
    transition: all 0.3s 1s ease-out;
}
.loaded #loader {
    opacity: 0;
    -webkit-transition: all 0.5s ease-out;
    -o-transition: all 0.5s ease-out;
    -moz-transition: all 0.5s ease-out;
    transition: all 0.5s ease-out;
}
svg#loader {
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    margin: 0 auto;
    height: 100%;
    width: 100%;
    z-index: 999;
    background: #ffffff;
}
svg:not(:root) {
    overflow: hidden;
}
#loader-wrapper .loader-section {
    position: fixed;
    top: 0;
    width: 51%;
    height: 100%;
    background: #ffffff;
    z-index: 99;
    -webkit-transform: translateX(0);
    -moz-transform: translateX(0);
    -ms-transform: translateX(0);
    -o-transform: translateX(0);
    transform: translateX(0);
}
```
