# Modules and connectors

## Mount points

A few standard mounts on the body, each the same mechanical pattern plus the same connector:
hip (legs, wheels or treads), shoulders (arms), back (backpack), head (sensors, camera).
Publish the pattern as a drawing and an SVG so anyone can cut or print an adapter.

## The connector

- Magnetic pogo-pin connector: snaps on, pulls off without damage, self-aligning.
- Pins: raw power, ground, and a shared bus (CAN for robustness and hot-plug tolerance, or I2C for
  simplicity), plus an "attached" detect pin.
- USB is possible (the body as a USB hub), but it is fussy to plug in and does not tolerate yanking.

## Wireless option

Each module carries a tiny Wi-Fi board (an ESP32), so a detached module still works and can be
reached over the network. On the body it uses the bus; off the body, Wi-Fi.

## One small protocol

Every module answers the same three questions, over the bus or over the network:
1. What are you? (type, version, maker)
2. What can you do? (a short list of actions and sensors)
3. Do this. (an action with parameters)

A new module works without special code for it.

## First module idea

A pan-tilt head for a camera: two stepper motors, a laser-cut frame, printed gears, a small driver
board. Useful on its own the day it works.
