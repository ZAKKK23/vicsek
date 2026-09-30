# plane-moving-targets-vicsek

A Vicsek-model agent simulation with moving targets, running in the browser with no dependencies and no build step.

## Model

- Neighbors are metric: every agent within radius **R** counts.
- Each agent's heading is the average heading of its neighbors (itself included), blended with the direction to its nearest target.
- The homing term is weighted by **ν · s**, where **ν** is the homing-vs-consensus weight and **s** is the homing strength.
- A uniform angular kick of size **η** is added every step.
- All agents move at the same constant speed **v0**.
- Targets: 0-5 straight-line targets on fixed-height lanes, plus one target oscillating asymmetrically in y (descends at frequency **q**, rises at **n·q**). All targets share one x-coordinate moving at speed **vx**.

## Run

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

## Deploy on GitHub Pages

Settings -> Pages -> Deploy from branch -> `main` / root.

## License

MIT
