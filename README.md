# main-web-redesign_draft

https://www.lib.uidaho.edu 

## Sprint issue tracking

- [drive folder](https://drive.google.com/open?id=1NTIBOM0k35Vn7QgKjK3EbGbxg3u2F3LK)
- [problem sheet](https://docs.google.com/spreadsheets/d/1YfBYW0g12v-_bgvRN9o8TwQSp_L__sEuxyHYISh_RXw/edit?usp=sharing)

## Assets Notes 

### Bootstrap 4.1

Bootstrap [components docs](https://getbootstrap.com/docs/4.1/components/alerts/)

### Fontawesome 5.0.13 free

[fontawesome cheatsheet](https://fontawesome.com/cheatsheet)

add icons in span, `<span class="fas fa-stroopwafel"></span>`.

All free icons are currently loaded. 
["regular" & "free" icons](https://fontawesome.com/icons?d=gallery&s=regular&m=free).

Could be loaded via two methods:

1. CSS + webfonts: traditional method, load webfonts. good with lots of icons on the page, simple, low CPU use.
2. JS + SVG: newer method, insert SVG icons using JS. good with fewer icons, higher CPU use.

Both methods are add the project, but it is using currently using CSS, check comments in `_includes/head.html`.

[Accessibility info](https://fontawesome.com/how-to-use/accessibility):

- JS + SVG version adds accessibility aria labels automatically. If the icon has semantic meaning, add a `title=` attribute to the fa `<span>`.
- CSS + webfonts version, need to add aria labels manually. 
    - decorative icons: add `aria-hidden` to element, e.g. `<span class="fas fa-camera-retro" aria-hidden></span>`
    - semantic icons: add `aria-hidden` and a `title` to element, plus add description with `class="sr-only"`.
