# 🎮 Gamem2D

A lightweight 2D game engine made with **C + Python**.

Gamem2D uses a DLL-based engine core written in C and a Python wrapper using `ctypes`, giving simple game creation while keeping good performance.

Current version: **0.5.2 Stable**

---

# ✨ Features

Current features:

- 🟩 Entity system
- 🎨 Custom background colors
- 🎮 Keyboard input
- 🧲 Collision system
- 🧱 Collision layers
- 📛 Entity names
- 🔍 Entity search (`find()`)
- ⚡ Velocity movement
- 📍 Position system
- 🪟 Custom window titles
- ⏱ Delta time
- 🔄 Main game loop system

---

# 📁 Project Structure

```text
Gamem2D/
│
├── gamem2d-build-0-5-2.c
├── gamem2d-build-0-5-2.dll
├── gamem2d.py
└── main.py

```

---

# ⚙ Requirements

Python:

- Python 3.10+
- ctypes (included with Python)

Compiler:

### not needed unless editing the c file
- GCC

---

# 🔨 Compiling

### dll comes with the project, use this if editing c file

Compile the DLL:

```bash
gcc gamem2d-build-0-5-1.c -shared -o gamem2d-build-0-5-1.dll -lgdi32 -luser32 -lkernel32
```

---

# 🚀 Quick Start

Example:

```python
import gamem2d

gamem2d.init()

gamem2d.set_title(
"Gamem2D Test"
)

gamem2d.set_background(
(60,140,255)
)

player=gamem2d.entity.create(
100,
100,
50,
50,
(0,255,0)
)

while gamem2d.running():

    speed=200

    vx=0
    vy=0

    if gamem2d.keypressed.key("d"):
        vx+=speed

    if gamem2d.keypressed.key("a"):
        vx-=speed

    if gamem2d.keypressed.key("w"):
        vy-=speed

    if gamem2d.keypressed.key("s"):
        vy+=speed

    gamem2d.entity.set_velocity(
    player,
    vx,
    vy
    )

    gamem2d.update()
```

---

# 📚 API

## Initialize engine

```python
gamem2d.init()
```

Creates the game window.

---

## Window title

```python
gamem2d.set_title(
"My Game"
)
```

---

## Background

```python
gamem2d.set_background(
(60,140,255)
)
```

---

## Create entity

```python
entity=gamem2d.entity.create(
x,
y,
width,
height,
(r,g,b)
)
```

Example:

```python
player=gamem2d.entity.create(
100,
100,
50,
50,
(0,255,0)
)
```

---

## Velocity

```python
gamem2d.entity.set_velocity(
entity,
vx,
vy
)
```

---

## Position

```python
gamem2d.entity.set_pos(
entity,
x,
y
)
```

Get position:

```python
x,y=gamem2d.entity.get_pos(
entity
)
```

---

## Layers

```python
gamem2d.entity.set_layer(
entity,
1
)
```

Objects only collide with entities on the same layer.

---

## Entity names

Set:

```python
gamem2d.entity.set_name(
entity,
"player"
)
```

Find:

```python
player=
gamem2d.entity.find(
"player"
)
```

---

## Collision

```python
if gamem2d.entity.collision(
player,
wall
):
    print("Collision")
```

---

# 🛣 Roadmap

## Gamem2D 0.5.3

Planned:

- 🖼 PNG sprites
- 🌄 Background images
- 🖱 Mouse improvements
- 🔤 Text rendering

---

## Gamem2D 0.6.0

Planned:

- 🔊 Audio system
- 🎬 Animation system
- 📦 Scene system

---

## Gamem3D

Planned:

- 🧊 3D objects
- 🎥 Camera system
- 💡 Lighting
- 🖼 Textures

---

# Created by

well just me (vetarentu56-web)

Gamem ecosystem:

- Gamem2D
- Gamem3D (planned)
