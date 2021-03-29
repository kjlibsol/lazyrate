# jquery.lazyrate.js

Jquery plugin designed to load images with a delay in between, to handle scenarios where loading images too fast would result in rate-limiting issues

# Pre-requisites

- include JQuery
- include jquery.lazyrate.js

# Usage

The images you want to lazyrate load, create their markup like this:

- Leave a placeholder in the src attribute (or leave it out)
- Put the path to the real image in data-src attribute
- Give the images a class (like lazyrate in this example)
 ```

    <img id="img001" data-src="img/IMG_0032.jpg" src="img/placeholder.png" height="200" class="lazyrate">
    <img id="img002" data-src="img/IMG_0037.jpg" src="img/placeholder.png" height="200" class="lazyrate">
    <img id="img003" data-src="img/IMG_0042.jpg" src="img/placeholder.png" height="200" class="lazyrate">
    
    <script>
        $(document).ready(function () {
            $(".lazyrate").lazyRate();
        });
    </script>
```
# Options



## Delay

Default delay between images loading is 200ms. To change it, specify a value in ms for delay, as shown here

```
    $(".lazyrate").lazyRate({
        delay: 500 //500ms between each image loading
    });
```  

