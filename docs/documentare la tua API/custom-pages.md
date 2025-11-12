---
title: Custom Pages
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

<Callout icon="👍" theme="okay">
  View this article as [a Custom Page](https://docs.readme.com/page/custom-page)
</Callout>

Custom Pages are great when you want to retain the top navigation of your ReadMe project, but also want a custom look below the search bar.

# What's different?

1. No left sidebar navigation
2. No table of contents on the right, even when headers are used
3. Different URL path (subfolder is /page instead of /docs)
4. No Suggested Edits
5. No page voting
6. No "updated x days ago"

<Callout icon="🚧" theme="warn">
  Custom Pages are not affected by versioning and are shared. If you delete a Custom Page it will be removed from everywhere.
</Callout>

# What's the same?

With a [dropdown subheader layout](/main/docs/subheader-layout), the Page Title appears in the breadcrumb navigation.

<Image align="center" border={true} width="smart" src="https://files.readme.io/14c46d5-Screen_Shot_2021-05-19_at_3.28.30_PM.png" className="border" />

> 📘 Note
>
> The Custom Page Title occupies the space of a Section in the breadcrumb navigation but it does **not** create a permanent Section in the drop-down menu.

## Modes

Custom Pages have two modes:

1. **Markdown:** The standard mode used in Documentation section

<Image border={true} src="https://files.readme.io/5300f08-CleanShot_2022-10-15_at_08.56.122x.png" className="border" />

2. **HTML:** The code is [sanitized](https://en.wikipedia.org/wiki/HTML_sanitization). If you want to include CSS or JavaScript, do so in Appearance > Custom Javascript/Stylesheet.
