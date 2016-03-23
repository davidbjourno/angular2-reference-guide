# Angular 2 reference guide

## File structure
```
my-app
├── app
│   └── app.component.js
│   └── main.js
├── index.html
├── license.md
```

## Components
* An Angular 2 **component** is a *JavaScript class* that controls a *view template*.
* Keep components code in `app/`.

### Component file
Example `app/app.component.js`:

```javascript
(function(app) { // Create single global namespace for application ("app"), pass into IIFE (Immediately-Invoked Function Expression)
  app.AppComponent = // Create visual component ("AppComponent"), export to "app" namespace
    ng.core.Component({ // "Component" method belonging to global Angular core namespace ("ng.core")
      selector: 'my-app',
      template: '<h1>My First Angular 2 App</h1>'
    })
    .Class({ // "Class" method belonging to global Angular core namespace
      constructor: function() {}
    });
})(window.app || (window.app = {})); // Initialise "app" with empty object if it doesn't already exist
```
