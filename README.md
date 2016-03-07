# Angular-touch

Angular UI + HTML5  that will let you create beautiful application which are based on touch and gesture.
The touch events are very helpful for the Mobile/Tablet application as well as Mobile/Tablet view.


# AngularJs Configuration

## Here is how to define your module has dependent on mobile-angular-ui

* touch/drag feature: this is from 'mobile-angular-ui.gestures.js'
* it is at a very beginning stage, so please be careful if you like to use
* in production. This is intended to provide a flexible, integrated and and 
* easy to use alternative to other 3rd party libs like hammer.js, with the
* final pourpose to integrate gestures into default ui interactions like 
* opening sidebars, turning switches on/off ..
  

```
var app = angular.module('MobileAngularUiExamples', [
  'ngRoute',
  'mobile-angular-ui',
  'mobile-angular-ui.gestures'
]);
app.run(function($transform) {
  window.$transform = $transform;
});

```

# AngularJs Routing
 
 * You can configure ngRoute as always, but to take advantage of SharedState location
 * in order to avoid unwanted routing.


```
app.config(function($routeProvider) {
  $routeProvider.when('/',              {templateUrl: '/demo/home.html', reloadOnSearch: false});
  $routeProvider.when('/touch',         {templateUrl: '/demo/touch.html', reloadOnSearch: false});
  $routeProvider.when('/swipe',         {templateUrl: '/demo/swipe.html', reloadOnSearch: false});
  $routeProvider.when('/drag',          {templateUrl: '/demo/drag.html', reloadOnSearch: false});
  $routeProvider.when('/drag2',         {templateUrl: '/demo/drag2.html', reloadOnSearch: false});
  $routeProvider.when('/carousel',      {templateUrl: '/demo/carousel.html', reloadOnSearch: false});
});

```

### By Tushar Khanjire
