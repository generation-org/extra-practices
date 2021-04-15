<img align="right" width="150" height="150" src="https://media-exp1.licdn.com/dms/image/C4E0BAQF7BYCCZt5epw/company-logo_200_200/0?e=2159024400&v=beta&t=qUAFP9bUgBEEXGVQYpUXW1J_OiP8e0r4rFBpqp8OrxA">

# React-Extra-01 - Tic tac toe

 <br/>

## Exercise

You will create a Tic Tac Toe game, with have the following steps: 

* The board is a 3X3 matrix
* On the first step, the first player selects one square on the board and mark it with an X
* On the second step, the next player selects another square at the board and mark it with an O
* On the following steps, the players take turns putting their marks in empty squares.
* The first player to get 3 of her marks in a row (up, down, across, or diagonally) is the winner.
* If the empty squares finish without any player marking three squares in a row, the game ends in a tie

Your game will follow the mentioned steps and have the following features:

1. It will indicate who should play next (X or O)
2. It will show a message one of the players wins, letting them know who won the game.
3. The players will be able to select a previous step of the game, see how the board was, and start to play from this step if they want. 

And, if you want an extra challenge, you can add those features to the game:

* Add a toggle button that allows the players to order the steps ascending or descending.
* Add the position chosed by the player on each step.
* Add a "reset" button, that can acionet at any step of the game
* Add a "play again" button, that will appear only when the game ends
* When the game ends in a tie, show a message informing the result

The goal here is to develop your React coding skills, so we provided the following HTML and CSS for your project, but feel free to create your own HTML and CSS as well!

#### HTML file:

```

<<div id="errors" style="
  background: #c00;
  color: #fff;
  display: none;
  margin: -20px -20px 20px;
  padding: 20px;
  white-space: pre-wrap;
"></div>
<div id="root"></div>
<script>
window.addEventListener('mousedown', function(e) {
  document.body.classList.add('mouse-navigation');
  document.body.classList.remove('kbd-navigation');
});
window.addEventListener('keydown', function(e) {
  if (e.keyCode === 9) {
    document.body.classList.add('kbd-navigation');
    document.body.classList.remove('mouse-navigation');
  }
});
window.addEventListener('click', function(e) {
  if (e.target.tagName === 'A' && e.target.getAttribute('href') === '#') {
    e.preventDefault();
  }
});
window.onerror = function(message, source, line, col, error) {
  var text = error ? error.stack || error : message + ' (at ' + source + ':' + line + ':' + col + ')';
  errors.textContent += text + '\n';
  errors.style.display = '';
};
console.error = (function(old) {
  return function error() {
    errors.textContent += Array.prototype.slice.call(arguments).join(' ') + '\n';
    errors.style.display = '';
    old.apply(this, arguments);
  }
})(console.error);
</script>

```

#### CSS file:

```

body {
  font: 14px "Century Gothic", Futura, sans-serif;
  margin: 20px;
}

ol, ul {
  padding-left: 30px;
}

.board-row:after {
  clear: both;
  content: "";
  display: table;
}

.status {
  margin-bottom: 10px;
}

.square {
  background: #fff;
  border: 1px solid #999;
  float: left;
  font-size: 24px;
  font-weight: bold;
  line-height: 34px;
  height: 34px;
  margin-right: -1px;
  margin-top: -1px;
  padding: 0;
  text-align: center;
  width: 34px;
}

.square:focus {
  outline: none;
}

.kbd-navigation .square:focus {
  background: #ddd;
}

.game {
  display: flex;
  flex-direction: row;
}

.game-info {
  margin-left: 20px;
}

```
