# RetroSnaker
js canvas
## 42行逆天代码，惊呆小伙伴，蛇可穿身，挑战千年不变的规则(ps:撞墙上还是GG的)
```javascript
  var canvas = document.getElementById('myCanvas')
        var ctx = canvas.getContext('2d');
        var snake = [286, 287, 288, 289, 290, 291];
        var f = 45,fo=100;
        function draw(i, c) {
            ctx.fillRect((i - 1) % 25 * 25, ~~((i - 1) / 25) * 25, 24, 24);
            ctx.fillStyle = c;
        }
        function go() {
            for (var i = 0; i < snake.length; i++) {
                draw(snake[i], "Black");
            }
        }          
            function main() {
                var c = document.getElementById("myCanvas");
                var cxt = c.getContext("2d");
                cxt.clearRect(0, 0, c.width, c.height); 
                if(!snake.indexOf(fo)){
                     snake.push(fo);
                     fo = Math.round(Math.random()*624+1);
                }else{
                      draw(fo,"Red");
                }
                document.onkeydown = function (event) {
                    var e = event || window.event;
                    if ((e.keyCode % 2 == 1) && (Math.abs(snake[0] -snake[1]) == 25)) {
                        snake.pop();
                        snake.unshift(snake[0] + e.keyCode - 38);
                        go();
                    } else if ((e.keyCode % 2 == 0) && (Math.abs(snake[0] -snake[1]) == 1)) {
                        snake.pop();
                        snake.unshift(snake[0] + (e.keyCode - 39) * 25);
                        go();
                    }
                };
                snake.pop();
                snake.unshift(snake[0] + snake[0] - snake[1]);
                if (snake[0]< 0 || snake[0]> 624 ||snake[0]%25==1&&snake[1]%25==0||snake[0]%25==0&&snake[1]%25==1||!snake.indexOf(snake[1])) {
                    alert("失败");
                }
                go();
            }
            setInterval("main()", 200);
```
