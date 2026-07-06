# Loquat

Keyboard for the Lenovo Legion Go (`loquat-legiongo`): a 207×130 mm board with tight-pitch PG1316S-style keys and an Azoteq TPS43 touchpad, designed with [Ergogen](https://ergogen.xyz).

## Layout / outlines

The Ergogen config lives in [`ergogen/config.yaml`](ergogen/config.yaml). To regenerate the outputs (points, outlines as SVG/DXF/PDF):

```sh
cd ergogen
npx --yes ergogen@latest ./config.yaml -o output --clean --debug
```

Requires Node.js; `npx` downloads the Ergogen CLI on first run. Results land in `ergogen/output/` — `output/outlines/preview.svg` is the quickest way to eyeball the result.

> `--clean` is not optional here. Without it, Ergogen re-ingests the `*.yaml` it previously wrote into `output/` and lets it override your edits to `config.yaml`, so changes silently appear to do nothing. `--debug` also dumps `output/points/points.yaml`, handy for checking a key's coordinates or whether it was skipped.
