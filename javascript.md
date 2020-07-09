# Client Side JS

## Detect Key Press

Information taken from [here](https://www.geeksforgeeks.org/jquery-keypress/).

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

## Moment

Formatting time

### HTML 

``` html
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.22.2/moment.min.js"></script>
```

### In JS

``` js
const timestamp = new Date().getTime()
// 24h clock
moment(timestamp).format('hh:mm')
// "Today is Sunday"
moment(timestamp).format("[Today is] dddd")
// "Sunday, February 14th 2010, 3:25:50 pm"
moment(timestamp).format("dddd, MMMM Do YYYY, h:mm:ss a")
```
