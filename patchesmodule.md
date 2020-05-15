# PatchesModule

`getBooleanValue`

`getBooleanValue(name: String): BoolSignal`

Returns a `BoolSignal` that is exported with `name` from the Patch Editor.

`getColorValue`

`getColorValue(name: String): RgbaSignal`

Returns a `RgbaSignal` that is exported with `name` from the Patch Editor.

`getPoint2DValue`

`getPoint2DValue(name: String): PixelPointSignal`

Returns a `PixelPointSignal` that is exported with `name` from the Patch Editor.

`getPointValue`

`getPointValue(name: String): PointSignal`

Returns a `PointSignal` that is exported with `name` from the Patch Editor.

`getPulseValue`

`getPulseValue(name: String): EventSource`

Returns a pulse `EventSource` that wrapps a pulse that is exported with `name` from the Patch Editor.

`getScalarValue`

`getScalarValue(name: String): ScalarSignal`

Returns a `ScalarSignal` that is exported with `name` from the Patch Editor.

`getStringValue`

`getStringValue(name: String): StringSignal`

Returns a `StringSignal` that is exported with `name` from the Patch Editor.

`getVectorValue`

`getVectorValue(name: String): VectorSignal`

Returns a `VectorSignal` that is exported with `name` from the Patch Editor.

`setBooleanValue`

`setBooleanValue(name: String, signal: BoolSignal): void`

Sends a `BoolSignal` that is imported with `name` into the Patch Editor.

`setColorValue`

`setColorValue(name: String, signal: ColorSignal): void`

Sends a `ColorSignal` that is imported with `name` into the Patch Editor.

`setPoint2DValue`

`setPoint2DValue(name: String, signal: PixelPointSignal): void`

Sends a `PixelPointSignal` that is imported with `name` into the Patch Editor.

`setPointValue`

`setPointValue(name: String, signal: PointSignal): void`

Sends a `PointSignal` that is imported with `name` into the Patch Editor.

`setPulseValue`

`setPulseValue(name: String, signal: EventSource): void`

Sends an `EventSource` that is imported with `name` into the Patch Editor.

Note: The `Reactive.once()` method can be used to return an `EventSource` that emits an empty event as soon as possible.

`setScalarValue`

`setScalarValue(name: String, signal: ScalarSignal): void`

Sends a `ScalarSignal` that is imported with `name` into the Patch Editor.

`setStringValue`

`setStringValue(name: String, signal: StringSignal): void`

Sends a `StringSignal` that is imported with `name` into the Patch Editor.

`setVectorValue`

`setVectorValue(name: String, signal: VectorSignal): void`

Sends a `VectorSignal` that is imported with `name` into the Patch Editor.

