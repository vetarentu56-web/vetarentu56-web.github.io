# Gamem Engine
a powerfull python / c engine for windows

## documentation
### creating a window

first, create a file called main.py
second, add this into the file

```python
import gamem2d

gamem2d.init()
gamem2d.set_title("My GameM2D Project")

while gamem2d.running():
  gamem2d.update()
```
### changing the background
```python
import gamem2d

gamem2d.init()
gamem2d.set_title("My GameM2D Project")

while gamem2d.running():
  gamem2d.set_background("20,40,80")
  gamem2d.update()
```
