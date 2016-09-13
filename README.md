* Now, add a property on scope called time which is equal to  ```currentTime.toString```
* If you did everything right reload your index.html page and you should see something like
```
  Hello, Tyler
  The current time is Sun Dec 07 2014 22:03:12 GMT-0700 (MST)
```
* If you don't see that, check your console and start debugging.
* Your final timeDirective.js file should look like this
```javascript
angular.module('timeApp').directive('showTime', function(){
  return {
    restrict: 'E',
    template: '<div> The current time is {{time}} </div>',
    link: function(scope, element, attrs){
      var currentTime = new Date();
      scope.time = currentTime.toString();
    }
  }
});
```

## Copyright

© DevMountain LLC, 2016. Unauthorized use and/or duplication of this material without express and written permission from DevMountain, LLC is strictly prohibited. Excerpts and links may be used, provided that full and clear credit is given to DevMountain with appropriate and specific direction to the original content.
