---
title: Links to Pages
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
## Internal Links

To create a link between pages, start by typing `[` and a scrollable menu of available pages to link to will appear. As you continue typing more characters, relevant internal page link options will appear.

<Image align="center" border={true} src="https://files.readme.io/cff6bf4-link_to_pages.gif" className="border" />

The resulting Markdown will look like this:

<Image align="center" border={true} src="https://files.readme.io/9b34336-CleanShot_2022-10-18_at_11.19.16.gif" className="border" />

And end up looking like the link above to users!

> 📘 Internal links only work within one project.
>
> If you link across multiple projects, you must use standard hyperlinks.

 

## Anchor Links

All section headers include an anchor link. The format is `#header-name`. So for example this [link](doc:linking-to-pages#anchor-links) will bring you back to this section:

```
[link](doc:linking-to-pages#anchor-links)
```

 

## External Links

### Inline Linking

To link inline, type the text you want to link within brackets, `[x]`, followed directly by the link URL within parentheses, `(y)`.

Links look like this in the Markdown editor:

```
[ReadMe](readme.com)
```

And result in a link that looks like this: [ReadMe](https://readme.com/)

 

### Reference-Style Linking

Reference-style linking allows you to give a link a number or "name" and refer to it multiple times.

For example, if you type the below in your dash:

```
When I first research something I look at [Wikipedia][1] then at [Google][2] then [Wookiepedia][3].

[1]: https://wikipedia.org            "Wikipedia"
[2]: https://google.com               "Google"
[3]: https://starwars.fandom.com      "Wookiepedia"
```

...the links will look like this in your Hub:

When I first research something I look at [Wikipedia][1] then at [Google][2] then [Wookiepedia][3].

[1]: https://wikipedia.org "Wikipedia"

[2]: https://google.com "Google"

[3]: https://starwars.fandom.com "Wookiepedia"

 

## Open Links in New Tab

Markdown and [RDMD](https://docs.readme.com/rdmd/docs/) currently do not have a way to define the target for a link. Instead, standard HTML will need to be used to open links in a new tab.

The HTML syntax is `target="_blank"`, which is used like this within the `<a>` tag:

```html
<a href="https://readme.com/" target="_blank">ReadMe</a>
```

This can be combined with our `doc:page` syntax to open [links to pages within the same project](doc:linking-to-pages#internal-links) like so:

```html
<a href="doc:intro-to-readme" target="_blank">Introduction</a>
```

 

## Validating Links

ReadMe supports several third-party tools to automatically find broken links in a documentation project, One service we suggest is the [W3C Validator](https://validator.w3.org/checklink). No login required. For the **URL** field, enter your doc's custom domain. Select **Hide redirects** and select **Check linked documents recursively**. Leave recursion depth blank.

The results will only show links that are broken, not on **which** pages those links occur, or how many times the broken links occur,

 

## What's Next

You can use the **What's Next** section at the bottom of the page to link to relevant pages within your project and/or relevant external links. You can also add a description to provide more context.

<Image align="center" border={true} src="https://files.readme.io/1ae72b6-New_Whats_Next.gif" className="border" />
