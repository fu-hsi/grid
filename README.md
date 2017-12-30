# FuGrid
Yet another simple and responsive grid system which I share after a few years.  
Let's call him FuGrid ;-)
## Compile
```
sass src/grid.scss dist/grid.css
```
## Minify
```
java -jar yuicompressor.jar -o '.css$:.min.css' dist/grid.css
```
## Example
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Grid example</title>
  <link rel="stylesheet" href="dist/grid.min.css">

  <style>
      * {
        -webkit-box-sizing: border-box;
           -moz-box-sizing: border-box;
                box-sizing: border-box;
      }
      
      .container {
          max-width: 980px;
          width: 100%;
          margin: 0 auto;
          padding: 0 10px;
      }
    </style>
</head>
<body>
  <div class="container">

    <div class="row">
      <div class="col-12">
        col-12
      </div>
    </div>

    <div class="row">
      <div class="col-3">
        col-3
      </div>
      <div class="col-3">
        col-3
      </div>
      <div class="col-3">
        col-3
      </div>
      <div class="col-3">
        col-3
      </div>
    </div>

  </div>
</body>
</html>

```
## Additional remarks
.container class is not a part of grid system, but it is used by him.  
If u change padding for .container, you should change $grid-gutter in scss too.

You can enable additional features:
- pull
- push

and add additional classes for specific devices (media):
```scss
@include media("super-small-devices", 320px);
```
then you can use it like this:
```html
<div class="super-small-devices-3">
```
For default we use:
```scss
@include media("", 480px);
```
without prefix.