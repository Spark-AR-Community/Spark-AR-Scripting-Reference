# TransformSignal

`position`

`(get) position: PointSignal (set) (Not Available)`

Represents the offset in the local coordinate system.

`rotationX`

`(get) rotationX: ScalarSignal (set) (Not Available)`

Represents rotation about the X-axis of the local coordinate system, in radians. The signal value is in the range \[-PI, PI\].

**Note**: The order of operations \(rotations in particular\) is the same as in `Transform`. The rotations are applied to the object in Z-Y-X order. The X rotation is applied first to the object, therefore it is always performed in the object's local coordinate system.

`rotationY`

`(get) rotationY: ScalarSignal (set) (Not Available)`

Represents rotation about the Y-axis of the rotated local coordinate system, in radians. The signal value is in the range \[-PI/2, PI/2\].

**Note**: The order of operations \(rotations in particular\) is the same as in `Transform`. The rotations are applied to the object in Z-Y-X order. The Y rotation is applied second to the object, therefore if the `rotationX` is not zero, then `rotationY` is applied not in the object's local coordinate system but in the rotated one.

`rotationZ`

`(get) rotationZ: ScalarSignal (set) (Not Available)`

Represents rotation about the Z-axis of the rotated local coordinate system, in radians. The signal value is in the range \[-PI, PI\].

**Note**: The order of operations \(rotations in particular\) is the same as in `Transform`. The rotations are applied to the object in Z-Y-X order. The Z rotation is applied last to the object, therefore if the `rotationX` or `rotationY` is not zero, then `rotationZ` is applied not in the object's local coordinate system but in the rotated one.

`scale`

`(get) scale: ScaleSignal (set) (Not Available)`

Represents scale in the local coordinate system.

`scaleX`

`(get) scaleX: ScalarSignal (set) (Not Available)`

Represents scale along the X-axis of the local coordinate system.

`scaleY`

`(get) scaleY: ScalarSignal (set) (Not Available)`

Represents scale along the Y-axis of the local coordinate system.

`scaleZ`

`(get) scaleZ: ScalarSignal (set) (Not Available)`

Represents scale along the Z-axis of the local coordinate system.

`x`

`(get) x: ScalarSignal (set) (Not Available)`

Represents the offset along the X-axis of the local coordinate system.

`y`

`(get) y: ScalarSignal (set) (Not Available)`

Represents the offset along the Y-axis of the local coordinate system.

`z`

`(get) z: ScalarSignal (set) (Not Available)`

Represents the offset along the Z-axis of the local coordinate system.

