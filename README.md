# RetroSnaker
js canvas
## 42行逆天代码，惊呆小伙伴，蛇可穿身，挑战千年不变的规则(ps:墙装上还是GG的)
```javascript

                if (snake[0] - snake[1] == (-25)) {
                    snake.pop();
                    snake.unshift(snake[0] - 25);
                }
                if (snake[0] - snake[1] == (25)) {
                    snake.pop();
                    snake.unshift(snake[0] + 25);
                }
                if (snake[0] - snake[1] == (-1)) {
                    snake.pop();
                    snake.unshift(snake[0] - 1);
                }
                if (snake[0] - snake[1] == (1)) {
                    snake.pop();
                    snake.unshift(snake[0] + 1);
                }
```
