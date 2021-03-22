<img align="right" width="150" height="150" src="https://media-exp1.licdn.com/dms/image/C4E0BAQF7BYCCZt5epw/company-logo_200_200/0?e=2159024400&v=beta&t=qUAFP9bUgBEEXGVQYpUXW1J_OiP8e0r4rFBpqp8OrxA">

# JS-Extra-01 - JavaScript Stopwatch

 <br/>

## Exercise

You will create a JavaScript stopwatch, with the following features: 

* Your stopwatch should have at least three buttons for user interaction:
  * Start
  * Stop
  * Reset
* The stop watch should show seconds and tens of seconds
* Button 'Start' should start the stopwatch. Tip: use Javascript's "setInterval" function to make the tens value increase every 10 milisseconds.
* Button 'Stop' should stop the timewatch. Tip: use JavaScript's "clearInterval" function
* Button 'Reset' should restart the count

The goal here is to develop your JavaScript coding skills, so we provided the following HTML and CSS for your project, but feel free to create your own HTML and CSS as well!

#### HTML file:

```

<!DOCTYPE html>
<html>
  <head>
    <meta charset=utf-8 />
    <title>JS Stopwatch</title>
  </head> 

  <body>
    <div class="wrapper">
      <h1>Stopwatch</h1>
      <h2>Vanilla JavaScript Stopwatch</h2>
      <p><span id="seconds">00</span>:<span id="tens">00</span></p>
      <button id="button-start">Start</button>
      <button id="button-stop">Stop</button>
      <button id="button-reset">Reset</button>
    </div> 
  </body>
</html>
```

#### CSS file:

```

/* Variabes */
/* Mixin's */
body {
  background: #ffa600;
  font-family: "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif;
  height: 100%;
}

.wrapper {
  width: 800px;
  margin: 30px auto;
  color: #fff;
  text-align: center;
}

h1, h2, h3 {
  font-family: "Roboto", sans-serif;
  font-weight: 100;
  font-size: 2.6em;
  text-transform: uppercase;
}

#seconds, #tens {
  font-size: 2em;
}

button {
  -moz-border-radius: 5px;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  -khtml-border-radius: 5px;
  background: #ffa600;
  color: #fff;
  border: solid 1px #fff;
  text-decoration: none;
  cursor: pointer;
  font-size: 1.2em;
  padding: 18px 10px;
  width: 180px;
  margin: 10px;
  outline: none;
}
button:hover {
  -webkit-transition: all 0.5s ease-in-out;
  -moz-transition: all 0.5s ease-in-out;
  transition: all 0.5s ease-in-out;
  background: #fff;
  border: solid 1px #fff;
  color: #ffa600;
}
```