# Insert JavaScript Code Inside HTML File
- Inside the ```<body>...</body>``` tags, add your JavaScript code inside ```<script>...</script>``` tags

## Example of JavaScript code inside HTML File
```html
<body>
    <script>
        console.log('hello');
        console.log('hi');
        alert('Hello World!');
    </script>
</body>
```

# Link a JavaScript File to an HTML file 

**NOTE:** This is the preferred method of running Javascript

- Create a JavaScript file with the .js extension
- Insert all of your JS code inside the .js file
- Link your .js file to your HTML file by referencing the local path to the file inside the script tag

## Example of Linking JavaScript File to HTML File
```html
<body>
    <script src='local/path/to/js/file.js'></script>
</body>
```