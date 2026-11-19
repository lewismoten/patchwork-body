# Power

## Cells and packs

- Source: a large stock of 18650 cells (about 300). Test every cell's capacity and internal resistance
  before use; build each pack only from matched, healthy cells.
- Packs are spot-welded, each with its own protection board (BMS) and a fuse.
- A standard pack format is a 4S pack (four cells in series: about 12 V empty to 16.8 V full), in a
  printed or laser-cut case with a keyed connector. Parallel groups (4S2P, 4S3P) for more runtime.

## Hot swap without losing power

- Two battery bays joined by an ideal-diode power path: the robot runs from the fuller pack, and either
  pack can be pulled while the other carries the load.
- A small buffer (supercapacitor or a tiny internal cell) covers the moment of the swap.
- The robot can swap its own packs at a dock: drop the empty one, pick up a charged one.
- With two packs, one can charge while the robot runs on the other.

## Rails

- **One raw rail everywhere:** the pack voltage (12–16.8 V) runs through every module connector.
- **Each module makes what it needs** with a small buck converter (around 90% efficient):
  12 V, 5 V, and 3.3 V (a small linear regulator after the 5 V buck is fine for low current).
- **Boost only when needed:** anything above pack voltage gets its own boost converter.
- **Optional power module** in the torso supplies ready-made 5 V and 12 V to simple attachments.
- **AC is not on the module bus.** If anything needs AC, it is its own module (an inverter, for example
  in a backpack) with a different, keyed connector that cannot mate with the low-voltage ones.

## Related project (separate)

A larger pack for THE CHEZ uses the same skills (cell testing, welding, protection) at car voltage and
current, which needs its own plan: proper fusing, a contactor, per-cell monitoring, an enclosure.
