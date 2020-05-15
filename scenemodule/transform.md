# Transform

`position`

`(get) position: PointSignal (set) position: PointSignal`

Specifies the object position along the X, Y and Z axis of the object's local coordinate system.

`rotation`

`(get) (Not Available) (set) rotation: Rotation`

Specifies the object rotation along the X, Y and Z axis of the object's local coordinate system.

`rotationX`

`(get) rotationX: ScalarSignal (set) rotationX: ScalarSignal`

Specifies the object rotation about the X-axis of the object's local coordinate system, in radians.

**Note**: the rotations are applied to the object in Z-Y-X order. The X rotation is applied first to the object, therefore it is always performed in the object's local coordinate system.

`rotationY`

`(get) rotationY: ScalarSignal (set) rotationY: ScalarSignal`

Specifies the object rotation about the Y-axis of the object's rotated local coordinate system, in radians.

**Note**: the rotations are applied to the object in Z-Y-X order. The Y rotation is applied second to the object, therefore if the `rotationX` is not zero, then `rotationY` is applied not in the object's local coordinate system but in the rotated one.

`rotationZ`

`(get) rotationZ: ScalarSignal (set) rotationZ: ScalarSignal`

Specifies the object rotation about the Z-axis of the object's rotated local coordinate system, in radians.

**Note**: the rotations are applied to the object in Z-Y-X order. The Z rotation is applied last to the object, therefore if the `rotationX` or `rotationY` is not zero, then `rotationZ` is applied not in the object's local coordinate system but in the rotated one.

`scale`

`(get) scale: ScaleSignal (set) scale: ScaleSignal`

Specifies the object scale along the X, Y and Z axis.

`scaleX`

`(get) scaleX: ScalarSignal (set) scaleX: ScalarSignal`

Specifies the object scale along the X-axis of the object's local coordinate system.

`scaleY`

`(get) scaleY: ScalarSignal (set) scaleY: ScalarSignal`

Specifies the object scale along the Y-axis of the object's local coordinate system.

`scaleZ`

`(get) scaleZ: ScalarSignal (set) scaleZ: ScalarSignal`

Specifies the object scale along the Z-axis of the object's local coordinate system.

`x`

`(get) x: ScalarSignal (set) x: ScalarSignal`

Specifies the object offset along the X-axis of the object's local coordinate system.

`y`

`(get) y: ScalarSignal (set) y: ScalarSignal`

Specifies the object offset along the Y-axis of the object's local coordinate system.

`z`

`(get) z: ScalarSignal (set) z: ScalarSignal`

Specifies the object offset along the Z-axis of the object's local coordinate system.

