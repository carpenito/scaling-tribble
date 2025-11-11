---
title: Create a Custom Component
description: >-
  Recipe DescriptioThis recipe walks through creating a simple reusable styled
  container that you can use throughout your documentation.


  Just wrap any content with ExampleComponent tags, and it will appear in a nice
  dark gray box!n
hidden: false
recipe:
  color: '#018FF4'
  icon: 🔧
---
```java Java
export const ExampleComponent = ({ children }) => {
  return (
    <div className="flex items-center h-full w-full">
      <div className="bg-gray-800 rounded-md p-6 m-4">
        {children}
      </div>
    </div>
  );
};

<ExampleComponent>
  Here's a very simple example component rather than an empty state. This should help you figure out what's happening quicker and see what's possible with custom components!
</ExampleComponent>
```

```json Response Example
{"success":true}
```

# Create an ExampleComponent

<!-- java@1 -->

We're creating a React component called ExampleComponent.

The export keyword makes this component available for import elsewhere

({ children }) uses destructuring to access any content placed between the component's opening and closing tags.

# Structuring the Component

<!-- java@2-8 -->

return (...) defines what the component will render, while the outer <div> uses Tailwind CSS classes to center its content and take up full width and height.

The inner <div> creates a dark gray box with rounded corners and padding

{children} is where the magic happens—this will render whatever content you place between your component tags.

# Using the Component

<!-- java@11-13 -->

The <ExampleComponent> opens the component.

The text between the tags becomes the children prop

Lastly, the </ExampleComponent> closes the component.