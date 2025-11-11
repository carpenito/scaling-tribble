---
title: Creating a Recipe
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Ready to transform your code samples into developer-friendly learning experiences? This guide walks you through building your first Recipe from start to finish. You'll learn how to break down complex code into digestible steps, add helpful annotations, and customize the visual experience to match your brand.

<br />

<Image align="center" border={false} src="https://files.readme.io/05e72a5519ad6e9421775f6688bbee366623e93528abf9df93dd5ae1973b81dd-Screenshot_2025-05-22_at_2.16.36_PM.png" />

<br />

## Before You Start

* Have your code sample ready (or know which API endpoint you want to use as a starting point)
* Ensure the Recipes section is accessible in your ReadMe project
* Consider what programming languages your developers use most
* Think about the key learning objectives for this particular code walkthrough

## Creating a Recipe

<Image border={false} src="https://files.readme.io/4482047-Screen_Shot_2020-12-01_at_3.42.35_PM.png" />

### 1. Access the Recipe Editor

Navigate to your ReadMe project and click **Edit** to enter the editing UI. From the main navigation, select **Recipes** to access the Recipe management area. Click the **Create New Recipe** button to launch the Recipe builder.

<Image align="center" border={false} src="https://files.readme.io/139f1a2224d1add344a0071284be7614929b7cac5be5babf7cb0860b16b9f81e-Screenshot_2025-05-22_at_12.47.08_PM.png" />

### 2. Configure Your Code Sample

1. In the upper right panel, select your programming language from the dropdown menu.
2. Add your code sample and make sure it's properly formatted with syntax highlighting. This will be the foundation that your step-by-step annotations will reference.

<Image align="center" border={false} src="https://files.readme.io/91f78f372bffaf5521f48ba6972275b5d3fa1b74cf4b4f917a5d7284a6d51c11-Screenshot_2025-05-22_at_2.09.51_PM.png" />

**Note:** Each Recipe can support multiple programming languages, so you can add additional language versions after setting up your first one.

### 3. Build Your Step-by-Step Annotations

In the left sidebar, create your highlighted steps that will guide developers through your code. For each step:

* Write a clear, descriptive title that explains what this part of the code accomplishes
* Add detailed explanations that help developers understand the "why" behind each section
* Specify the line numbers that should be highlighted for this step
* Use conversational language that makes complex concepts approachable

Each step should focus on a specific concept or action within your code sample, building understanding progressively.

<Image border={false} src="https://files.readme.io/cece453-Screen_Shot_2020-12-01_at_3.49.54_PM.png" />

### **4. Add Response Examples**

In the lower right panel, include the expected API response when your code runs successfully. This shows developers exactly what success looks like and helps them verify their implementation.

If your code doesn't generate a response (or if showing one isn't relevant), you can leave this section empty—it will automatically hide from the final Recipe.

**Note:** User data variables work in Recipes too! If you have personalized docs set up, you can include dynamic content in your responses.

> 👍 User data variables work in Recipes!
>
> If you have [variables](doc:personalized-docs) in your documentation, for example passed in via the Personalized Docs Webhook, they'll work in Recipes too!

### 5. Customize Visual Appearance

Switch to the **Appearance** tab to make your Recipe uniquely yours:

* **Select an emoji**: Click the emoji icon to choose from the dropdown menu
* **Set background color**: Use the color picker to select a background that matches your brand (supports RGB, HSL, or HEX values)
* **Write a description**: Add a detailed description that will appear on the larger Recipe card in your Recipes section

The _Open Recipe_ button color automatically inherits from your project's link color settings.

<Image border={false} src="https://files.readme.io/ea6500f-Screen_Shot_2020-10-19_at_12.41.19_PM.png" />

### **6. Choose Embedding Locations**

Decide where your Recipe should appear throughout your documentation:

* **API Reference embedding**: Select specific endpoints where this Recipe provides relevant context
* **Recipes section**: Your Recipe will automatically appear in the main Recipes area once published
* **Guide embedding**: You can manually embed the Recipe into guide pages later using the Recipe widget

Select the checkboxes next to relevant endpoints to make your Recipe accessible exactly where developers need it most.

The Recipe will appear as a clickable card as shown in the preview area of the Appearance step.

<Image border={false} src="https://files.readme.io/20cf1e2-Screen_Shot_2020-12-03_at_5.14.16_PM.png" />

<br />

<Image border={false} src="https://files.readme.io/e4619b5-Screen_Shot_2020-12-01_at_2.59.43_PM.png" />

<br />

<Callout icon="🚧" theme="warn">
  Embeds will not appear in the Reference section [until the Recipes section is enabled](#enable-recipes-section).
</Callout>

<br />

### 7. Set Publication Status

Choose your Recipe's visibility level:

* **Unpublished**: Only visible to project administrators (default for new Recipes)
* **Published**: Visible to all users in your Recipe collection
* **Featured**: Showcased prominently at the top of your Recipes section (only one Recipe can be featured at a time)

Start with "Published" to make your Recipe available to developers, or keep it "Unpublished" while you're still refining the content.

|                 |                                                                                                                                                                 |
| :-------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Featured**    | This is the showcased Recipe at the top of the Recipe section. One Recipe must be featured if your Recipes page is public, and it must be in a published state. |
| **Published**   | Visible to users in the card grid below the featured Recipe                                                                                                     |
| **Unpublished** | Cannot be seen by customers. New Recipes are unpublished by default.                                                                                            |

<Image border={false} src="https://files.readme.io/445d0c8-Screen_Shot_2020-12-16_at_3.54.22_PM.png" />

<br />

## FAQ & Troubleshooting

**Can I remove the Recipe icon in the nav bar?**

This section is only visible to project admins. Your customers will not see this section unless you [enable it](#enabling-your-recipes-page) to make it visible to them.

As we transition more editing capabilities to the frontend of your docs hub, we'll continue to make it clearer what project admins see versus what your customers see.

**How do I change the color of the blue "Open Recipe" button?**

This button color is inherited from the Link Color you've set in the [Theme Editor](/main/docs/design-themes) in your project settings. To change it, you will need to change the Link Color for your entire ReadMe hub.

**Can I rename the Recipe section like the other sections?**

Not yet, but we're working on it!

**My code highlighting isn't working correctly?** Double-check that your line numbers are accurate and that you've selected the correct programming language. Remember that line numbers start from 1, not 0.

**The Recipe widget doesn't appear in my guides?** Make sure the Recipes section is enabled in your site navigation settings. The widget won't be available until Recipes are activated for your project.

**My embedded Recipe isn't showing up in API Reference pages?** Embedded Recipes only appear once the Recipes section is publicly enabled. Check your site navigation settings and ensure at least one Recipe is published.

**The response section disappeared?** If you clear the default response content completely, the response panel will automatically hide. Add content back to make it visible again.
