# ps-facebook-pixel
AngularJS lazy load youtube video

## Usage
  -load js
  ```html
  <script src="./angular.js"></script>
  <script src="./angular-facebook-pixel.min.js"></script>
  ```

  -module
  ```js
  angular.module('MyApp', ['ps-facebook-pixel'])
  ```
## Config
  ```js
  myApp.config(function($pixelProvider) {
    $pixelProvider.id = '1234567890'; // required, pixel id
    $pixelProvider.currency = 'TWD'; // options, default is TWD!
    $pixelProvider.disablePushState = false; // options, default is false
    $pixelProvider.delayPageView = false; // options, default is false
  })
  ```

## Manual PageView
  ```js
  myApp.run(function($pixel) {
    $pixel.pageView();
  })
  ```

## Track
  ```js
  $pixel.track('AddToCart', {
    content_ids: ['1234', '1853', '9386'],
    content_type: 'product',
    value: 67,
    currency: 'TWD'
  })
  ```
    
## Purchase
  ```js
  $pixel.purchase(67);
  <!--- or --->
  $pixel.purchase({
    value: 67,
    currency: 'TWD'
  });
  ```
