# Link an External CSS Style Sheet to HTML File
- Use the `<link rel="stylesheet" href="mystyle.css">` tag inside the `<head></head>` section of the HTML file
- This should be the last item in the head section

```html
<head>
    <link rel="stylesheet" href="mystyle.css">
</head>
```

# Add CSS Directly to HTML
**NOTE:** This is not recommended, keep CSS seperate from HTML

- Insert the CSS between `<style></style>` tags
- Insert the `<style></style>` tags  inside the `<head></head>` section of the HTML file

```html
<head>
    <style>
        /* Insert CSS HERE */
    </style>
</head>
```