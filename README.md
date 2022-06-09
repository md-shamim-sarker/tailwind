
# Tailwind CSS

A utility-first CSS framework packed with classes like flex, pt-4, text-center and rotate-90 that can be composed to build any design, directly in your markup.



## Official Website

[https://tailwindcss.com/](https://tailwindcss.com/)

## Tailwind CSS Cheatsheet

- [https://tailwindcomponents.com/cheatsheet/](https://tailwindcomponents.com/cheatsheet/)
- [https://nerdcave.com/tailwind-cheat-sheet](https://nerdcave.com/tailwind-cheat-sheet)






## Necessary Extensions for Tailwind CSS
- Tailwind CSS IntelliSense
- Live Server

## Installation

Install Tailwind CSS project using Node.js and VS Code Editor.

- Create a folder at a preferable location (D:\GitLab\tailwindcss)
- Open VS Code Editor
- Open project folder through VS Code (File/Open Folder.../)
- Create folder named (.vscode, dist and src) in project root folder
- Create settings.json inside .vscode folder and copy this script
```bash
{
    "css.validate": false,
    "tailwindCSS.emmetCompletions": true
}
```
- Create output.css inside dist folder
- Create input.css inside src folder and copy this script
```bash
@tailwind base;
@tailwind components;
@tailwind utilities;
```
- Create index.html file in project root folder and copy this boiler plate
```bash
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
- Go to Terminal and initialize npm to generate package.json
```bash
npm init -y
```
- Inside package.json replace this script from "test": "echo \"Error: no test specified\" && exit 1" to
```bash
"build": "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
```
- Go to Terminal to install and initialize tailwindcss
```bash
npm install -D tailwindcss
npx tailwindcss init
```
- After run this two command, node_modules folder, package-lock.json and tailwind.config.js are generated
- Modify tailwind.config.js file like this
```bash
module.exports = {
  content: ["*.*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
- Got to Terminal and run this command
```bash
npm run build
```
- Must be Rebuilding... are seen on Terminal and the Tailwindcss environment is ready to development

# Tailwindcss aspect-ratio plugin installation
```bash
npm install @tailwindcss/aspect-ratio
```
## Modify tailwind.config.js file like this
```bash
module.exports = {
  content: ["*/*.html"],
  theme: {
    extend: {},
  },
  plugins: [require('@tailwindcss/aspect-ratio')],
}
```