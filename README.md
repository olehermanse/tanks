# Tanks

A small browser game where four tanks, each driven by a JavaScript snippet you can edit in the page, fight on a top-down grid.

You can play it here:

https://tanks.oleherman.com/

## Run locally without Docker

This application works without any server running, just open `index.html` in a browser.

## Run with Docker

```sh
docker build -t tanks . && docker run --rm -p 8080:80 tanks
```

## How to play

Each editor holds the body of a function that is called once per round with `me`, `enemy`, `enemies`, `bullets` and `grid`.
The first line must declare the AI's name, for example `const NAME = "My Bot";`, and the function must return an array of two actions from `"left"`, `"right"`, `"forward"` and `"fire"`.
Press **Play** to lock the editors and run the match. The last tank standing wins.

## License

See [LICENSE](LICENSE).

## Disclaimer

This app was written with the help of AI / LLMs (Claude Code + Fable 5.1).
The source code lives at <https://github.com/olehermanse/tanks>.
