# WorldTransform

`position`

`(get) position: PointSignal (set) position: PointSignal`

Specifies the object position along the X, Y and Z axis of the world coordinate system.

`rotationX`

`(get) rotationX: ScalarSignal (set) (Not Available)`

Represents rotation about the X-axis of the world coordinate system, in radians. The signal value is in the range \[-PI, PI\].

**Note**: The order of operations \(rotations in particular\) is the same as in `Transform`. The rotations are applied to the object in Z-Y-X order. The X rotation is applied first to the object.

`rotationY`

`(get) rotationY: ScalarSignal (set) (Not Available)`

Represents rotation about the Y-axis of the world coordinate system, in radians. The signal value is in the range \[-PI, PI\].

**Note**: The order of operations \(rotations in particular\) is the same as in `Transform`. The rotations are applied to the object in Z-Y-X order. The Y rotation is applied second to the object, therefore if the `rotationX` is not zero, then `rotationY` is applied not in the object's local coordinate system but in the rotated one.

`rotationZ`

`(get) rotationZ: ScalarSignal (set) (Not Available)`

Represents rotation about the Z-axis of the world coordinate system, in radians. The signal value is in the range \[-PI, PI\].

**Note**: The order of operations \(rotations in particular\) is the same as in `Transform`. The rotations are applied to the object in Z-Y-X order. The Z rotation is applied last to the object, therefore if the `rotationX` or `rotationY` is not zero, then `rotationZ` is applied not in the object's local coordinate system but in the rotated one.

`scale`

`(get) scale: ScaleSignal (set) (Not Available)`

Represents scale in the world coordinate system.

`scaleX`

`(get) scaleX: ScalarSignal (set) (Not Available)`

Represents scale along the X-axis of the world coordinate system.

`scaleY`

`(get) scaleY: ScalarSignal (set) (Not Available)`

Represents scale along the Y-axis of the world coordinate system.

`scaleZ`

`(get) scaleZ: ScalarSignal (set) (Not Available)`

Represents scale along the Z-axis of the world coordinate system.

`x`

`(get) x: ScalarSignal (set) (Not Available)`

Represents the offset along the X-axis of the world coordinate system.

`y`

`(get) y: ScalarSignal (set) (Not Available)`

Represents the offset along the Y-axis of the world coordinate system.

`z`

`(get) z: ScalarSignal (set) (Not Available)`

Represents the offset along the Z-axis of the world coordinate system.

