---
title: Custom CSS & JavaScript
deprecated: false
hidden: false
metadata:
  robots: index
---
In this section you can add CSS and Javascript to further customize the appearance of your docs site.

<Image align="center" border={true} src="https://files.readme.io/ca07f17-CleanShot_2022-09-25_at_09.57.452x.png" className="border" />

> 🚧 Selectors
>
> Use `.rm-` prefixed selectors. Hashed selectors change constantly and **should not** be relied on as selectors (ie. `Header-bottom2eLKOFXMEmh5`).

## Custom Stylesheet

<Callout icon="📘" theme="info">
  You should limit your changes to minor tweaks. Additionally, stylesheets aren't versioned; all versions use the same stylesheet.
</Callout>

## Custom Javascript

Your Javascript will be included at the bottom of the page.

<details>
  <summary><b>Global Variables</b></summary>

  ReadMe exposes certain global variables to help you customize the user experience of your hub:

  * **`RM_ReferenceSidebarScrollTopOffset`**\
    Pixel offset for the scroll-to-active-item sidebar logic in continuous <Glossary>Reference</Glossary> sections.
</details>

## Custom Include Tags

**Header HTML**

Any html here will be included in the head tag, which is good for things like meta tags and loading external CSS or JS.

**Footer HTML**  
​  
This will go right before the `</body>` tag. Good for things like analytics and tracking.

## Toggling Custom Javascript and CSS

Add the `?disableCustomCss=true&disableCustomJs=true` query params to the end of any URL.
