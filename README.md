## W3Data Library Study

```
<!DOCTYPE html>
<html>
<!-- W3Data Library -->
<script src="http://www.w3schools.com/lib/w3data.js"></script>

<body>

<div w3-include-html="content.html"></div>

<script>
// Execute w3-include-html statement.
w3IncludeHTML();
</script>

</body>
</html>
```

## HTML5 Import Template(Firefox no support)

```
<head>
    <title></title>
    <link rel="import" href="sample02_template01.html">
</head>
<body>
    <script>
        function supportsImports() {
          return 'import' in document.createElement('link');
        }

        if (supportsImports()) {
          // Good to go!
          console.log('Support import attribute!');
          var allocNode = document.querySelector('link[rel="import"]').import.querySelector('.template01').cloneNode(true);
          document.body.appendChild(allocNode);
        } else {
          // Use other libraries/require systems to load files.
          console.log('No Support import attribute!');
        }
    </script>
</body>
```
