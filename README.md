# Patchwork body

Ideas for a small, modular home robot: pieces that each work on their own and patch together into a
body. Anyone should be able to build a better hand, arm, legs, tank treads or a backpack and swap it on.

Status: ideas only. Nothing here has been built or tested.

## Goals

- **Cheap and easy to build and assemble.** Common parts, hand tools, a laser cutter, a 3D printer
  and a sewing machine. No custom boards unless they're optional.
- **Modular.** Standard mount points and one connector for power and data. A module is useful
  on its own and works the moment it is attached.
- **Small and friendly.** Child-sized at most, and clearly a machine. Nothing that could be mistaken
  for a person.
- **Gets around the house.** Stable enough not to be pushed over by a large dog; low and wide,
  wheels or treads before legs.
- **Runs itself.** It can connect and disconnect its own modules, swap its own battery packs without
  losing power, and drive onto a charging dock.

## Docs

- [Power](docs/power.md): battery packs, hot swap, voltage rails
- [Modules and connectors](docs/modules.md): mount points, the shared bus, how modules announce themselves
- [Locomotion](docs/locomotion.md): wheels, treads, legs; staying upright
- [Safety](docs/safety.md): lithium cells, AC, pets
- [Open questions](docs/questions.md)

## Viewer

`viewer/index.html` is a three.js model of the current idea: base, battery bays, torso, head and the mount
points. Open it in a browser (it loads three.js from a CDN). Click a part to see what it is; the
Explode button pulls the modules apart.

## Credits

Ideas by Lewis Moten, written up with Claude (Anthropic) from a conversation on 2026-11-18.
