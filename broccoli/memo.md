# lsystem examples 

## dragon

productions 2
FX
X: X/YF/
Y: \FX\Y

## koch

F++F++F
F: F-F++F-F
angle 30

## broccoli

productions 2
X
X → F[*|+FY]/(@%X)
Y → F[*|+FZ]/(@%Y)
Z → F[*|+FO]/(@%Z)
iterations 7
pitch 137.5
yaw 42.5

- productions: 3
- iterations: 7

## memo

notation from http://michelanders.blogspot.com/p/creating-blender-26-python-add-on.html
+, - rotate around the right axis (pitch)
/, \\ rotate around the up axis (yaw)
<, > rotate around the forward axis (roll)

notation from "Using L-Systems to Simulate the Romanesco Broccoli"

```
X → F[∧FX]+{X}
ω :A
A → F[∧GB]+{A}
B → F[∧GC]+{B}
C → F[∧GO]+{C}

+ Turn left by angle δ, using rotation matrix RU(δ). (yaw)
- Turn right by angle δ, using rotation matrix RU(−δ). (yaw)
& Pitch down by angle δ, using rotation matrix RL(δ). (pitch)
∧ Pitch up by angle δ, using rotation matrix RL(−δ). (pitch)
\ Roll left by angle δ, using rotation matrix RH(δ). (roll)
/ Roll right by angle δ, using rotation matrix RH(−δ) (roll)
```
