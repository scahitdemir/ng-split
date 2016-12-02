# Ng-Split

This angular directive is wrapper for [Split.js](http://nathancahill.github.io/Split.js/) and also this directive was inspired by [ng2-split](https://bertrandg.github.io/ng2-split//)

## Download Ng-Split

You can install ng-split via npm and Bower and its dependencies will be downloaded
automatically:

#### Npm
```bash
$ npm install ng-split --save
```

#### Bower
```bash
$ bower install ng-split --save
```

## Inject the Ng-Split Directive
- Add ng-split.min.js to your main file (index.html).

- Set `ng-split` as a dependency in your module
```javascript
var myapp = angular.module('myapp', ['ng-split'])
```

##HTML
####Horizontal Split
```javascript
<split direction="horizontal">
    <split-area size="50">
        <p>Lorem ipsum dolor sit amet...</p>
    </split-area>
    <split-area size="50">
        <p>Sed ut perspiciatis unde omnis iste natus erro...</p>
    </split-area>
</split>
```

####Vertical Split
```javascript
<split direction="vertical">
    <split-area size="25">
        <p>Lorem ipsum dolor sit amet...</p>
    </split-area>
    <split-area size="75">
        <p>Sed ut perspiciatis unde omnis iste natus erro...</p>
    </split-area>
</split>
```

####Multiple Split
```javascript
<split direction="horizontal">
    <split-area size="40">
        <split direction="vertical">
            <split-area size="30">
                <p>Lorem ipsum dolor sit amet...</p>
            </split-area>
            <split-area size="40">
                <p>Sed ut perspiciatis unde omnis iste natus erro...</p>
            </split-area>
            <split-area size="30">
                <p>Lorem ipsum dolor sit amet...</p>
            </split-area>
        </split>
    </split-area>
    <split-area size="60">
        <split direction="vertical">
            <split-area size="50">
                <p>Lorem ipsum dolor sit amet...</p>
            </split-area>
            <split-area size="50">
                <p>Sed ut perspiciatis unde omnis iste natus erro...</p>
            </split-area>
        </split>
    </split-area>
</split>
```

##CSS
```css
  .split p {
    padding: 20px;
  }

  .split {
    -webkit-box-sizing: border-box;
       -moz-box-sizing: border-box;
            box-sizing: border-box;

    overflow-y: auto;
    overflow-x: hidden;
  }

  .gutter {
    background-color: #eee;

    background-repeat: no-repeat;
    background-position: 50%;
  }

  .gutter.gutter-horizontal {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAUAAAAeCAYAAADkftS9AAAAIklEQVQoU2M4c+bMfxAGAgYYmwGrIIiDjrELjpo5aiZeMwF+yNnOs5KSvgAAAABJRU5ErkJggg==');
    cursor: ew-resize;
  }

  .gutter.gutter-vertical {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAFCAMAAABl/6zIAAAABlBMVEUAAADMzMzIT8AyAAAAAXRSTlMAQObYZgAAABRJREFUeAFjYGRkwIMJSeMHlBkOABP7AEGzSuPKAAAAAElFTkSuQmCC');
    cursor: ns-resize;
  }

  .split.split-horizontal, .gutter.gutter-horizontal {
    height: 100%;
    float: left;
  }
```
