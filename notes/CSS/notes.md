
For better type-safety, we recommend Prisma or Drizzle, which automatically generates types based on your database schema.

#### CSS Modules
CSS Modules allow you to scope CSS to a component by automatically creating unique class names, so you don't have to worry about style collisions as well.
Provide a way to make CSS classes locally scoped to components by default, reducing the risk of styling conflicts.

### [clsx](https://www.npmjs.com/package/clsx)
clsx is a library that lets you toggle class names easily. We recommend taking a look at documentation for more details, but here's the basic usage:


#### [SASS ](https://www.w3schools.com/sass/sass_intro.asp)
SASS (Syntactically Awesome Stylesheets) is a powerful CSS preprocessor that extends the capabilities of CSS, providing additional features to make writing styles easier, more maintainable, and more efficient.

##### Key Features of SASS

1. **Variables**: Store reusable values like colors, fonts, or sizes.

2. **Nesting**: Write CSS rules in a hierarchical structure that mirrors the HTML layout.

3. **Partials and Import**: Break styles into smaller, modular files and import them into a main file.

4. **Mixins**: Define reusable blocks of styles that can accept arguments for customization.

5. **Inheritance (Extends)**: Share styles between selectors using the `@extend` directive.

6. **Mathematical Operations**: Perform calculations directly in styles (e.g., for widths, margins, paddings).

7. **Functions**: Use built-in or custom functions for dynamic styles (e.g., color manipulation).

### How Does Sass Work?
A browser does not understand Sass code. Therefore, you will need a Sass pre-processor to convert Sass code into standard CSS.

This process is called transpiling. So, you need to give a transpiler (some kind of program) some Sass code and then get some CSS code back.