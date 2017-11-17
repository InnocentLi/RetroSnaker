# RetroSnaker
js canvas

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
