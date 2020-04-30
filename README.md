# Patrick's Project(Using React, Material UI,Firebase)
1. Re-code by me
* Source video:
> https://www.youtube.com/watch?v=I250xdtUvy8
2. Bonus
* Debounce (high-order function):

      // Returns a function, that, as long as it continues to be invoked, will not
      // be triggered. The function will be called after it stops being called for
      // N milliseconds. If 'immediate' is passed, trigger the function on the
      // leading edge, instead of the trailing.
      function debounce(func, wait, immediate) {
        var timeout;
        return function() {
          var context = this, args = arguments;
          var later = function() {
            timeout = null;
            if (!immediate) func.apply(context, args);
          };
          var callNow = immediate && !timeout;
          clearTimeout(timeout);
          timeout = setTimeout(later, wait);
          if (callNow) func.apply(context, args);
        };
      };


      var myEfficientFn = debounce(function() {
      // All the taxing stuff you do
      }, 250);

      window.addEventListener('resize', myEfficientFn);

* Remove HTML Tag:
      function removeHTMLTags (str) {
        return str.replace(/<[^>]*>?/gm, '');
      } 