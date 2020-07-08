# Client Side JS

## Detect Key Press

### HTML

``` html

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"> </script>

```

### In JS

``` js
$(document).keypress(function(e){ 
    if(e) {
      console.log('pressed' ,e.which)
    }
})
```
