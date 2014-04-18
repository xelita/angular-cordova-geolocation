angular-cordova-geolocation
===========================

Bring Apache Cordova Geolocation API to AngularJS Apps...

Define a simple service to deal with Cordova Geolocation Plugin (https://github.com/apache/cordova-plugin-geolocation).

[![Build Status](https://travis-ci.org/xelita/angular-cordova-geolocation.png?branch=master)](https://travis-ci.org/xelita/angular-cordova-geolocation)

Usage
-----
Include cordovaGeolocationModule.js in your Cordova application.

```html
<script src="js/cordovaGeolocationModule.js"></script>
```

or use the minified version:

```html
<script src="js/cordovaGeolocationModule.min.js"></script>
```

Add the module `cordovaGeolocationModule` as a dependency to your app module:

```js
var myapp = angular.module('myapp', ['cordovaGeolocationModule']);
```

Use the cordovaGeolocationModule as controller dependency and call cordovaGeolocationModule API:

```js
$scope.getCurrentPosition = function() {
    cordovaGeolocationService.getCurrentPosition(function(position){
        alert(
            'Latitude: '          + position.coords.latitude          + '\n' +
            'Longitude: '         + position.coords.longitude         + '\n' +
            'Altitude: '          + position.coords.altitude          + '\n' +
            'Accuracy: '          + position.coords.accuracy          + '\n' +
            'Altitude Accuracy: ' + position.coords.altitudeAccuracy  + '\n' +
            'Heading: '           + position.coords.heading           + '\n' +
            'Speed: '             + position.coords.speed             + '\n' +
            'Timestamp: '         + position.timestamp                + '\n'
        );
    });
};
```

Sample
------
A sample based on Ionic Framework can be found here:
https://github.com/xelita/angular-cordova-plugins-sample