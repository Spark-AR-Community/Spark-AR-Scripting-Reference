# Face

`cameraTransform`

`(get) cameraTransform: TransformSignal (set) (Not Available)`

Specifies a `TransformSignal` object describing the face transformation relative to camera coordinate system.

**Note**: `cameraTransform.applyTo(point)`, where `point` is a point in face local coordinate system, returns a point in camera local coordinate system.

`chin`

`(get) chin: Chin (set) (Not Available)`

Specifies a `Chin` object describing the attributes of the chin.

`forehead`

`(get) forehead: Forehead (set) (Not Available)`

Specifies a `Forehead` object describing the attributes of the forehead.

`id`

`(get) id: StringSignal (set) (Not Available)`

Specifies a `StringSignal` containing the unique ID assigned to a face. An ID is generated every time a face is detected and tracked in the scene.

When a face is lost and then tracked again, a new ID is generated even if it is the same person.

`isTracked`

`(get) isTracked: BoolSignal (set) (Not Available)`

A `boolSignal` indicating whether the face was tracked this frame.

If the face was not tracked, other properties represent the most recent tracked frame.

`leftCheek`

`(get) leftCheek: Cheek (set) (Not Available)`

Specifies a `Cheek` object describing the attributes of the left cheek.

`leftEye`

`(get) leftEye: Eye (set) (Not Available)`

Specifies an `Eye` object describing the attributes of the left eye.

`leftEyebrow`

`(get) leftEyebrow: Eyebrow (set) (Not Available)`

Specifies an `Eyebrow` object describing the attributes of the left eyebrow.

`mouth`

`(get) mouth: Mouth (set) (Not Available)`

Specifies a `Mouth` object describing the attributes of the mouth.

`nose`

`(get) nose: Nose (set) (Not Available)`

Specifies a `Nose` object describing the attributes of the nose.

`rightCheek`

`(get) rightCheek: Cheek (set) (Not Available)`

Specifies a `Cheek` object describing the attributes of the right cheek.

`rightEye`

`(get) rightEye: Eye (set) (Not Available)`

Specifies an `Eye` object describing the attributes of the right eye.

`rightEyebrow`

`(get) rightEyebrow: Eyebrow (set) (Not Available)`

Specifies an `Eyebrow` object describing the attributes of the right eyebrow.

