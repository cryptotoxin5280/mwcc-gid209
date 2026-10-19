# WordPress Theme Structure

A WordPress theme is just a collection of HTML, CSS, JSON, and PHP files.

```text
wp_theme_structure
├── README.txt
├── functions.php
├── parts
│   ├── footer.html
│   └── header.html
├── patterns
│   └── example.php
├── screenshot.png
├── style.css (REQUIRED)
├── styles
│   └── example.json
├── templates
│   ├── 404.html
│   ├── archive.html
│   ├── index.html (REQUIRED)
│   └── singular.html
└── theme.json
```
### Required Files

- `style.css` (Main Stylesheet) : Configuring Theme Data and adding Custom CSS.

- `templates/index.html` : Default/Fallback template; Defines this as a WordPress Block Theme.

***