# PointSignal

`abs`

`abs(): ScalarSignal`

Returns a signal with the value that is the absolute value of the given signal.

**See Also**: `ReactiveModule.abs`

`add`

`add(other: ScalarSignal): ScalarSignal add(other: VectorSignal): PointSignal add(other: VectorSignal): VectorSignal add(other: PointSignal): PointSignal`

Returns a signal with the value that is the sum of the values of the given signals.

**Note**: `add` and `sum` functions are synonyms, the behavior they provide is equivalent.

**See Also**: `ScalarSignal.sum`, ReactiveModule.add\`

`atan2`

`atan2(other: ScalarSignal): ScalarSignal`

Returns a signal with the value that is the angle in radians between the x-axis and the ray from \(0, 0\) to \(x, y\) where x and y are the values of the specified signals. The range is -PI to +PI.

**See Also**: `ReactiveModule.atan2`

`ceil`

`ceil(): ScalarSignal`

Returns a signal with the value that is the smallest integer that is greater than or equal to the value of the given signal.

**See Also**: `ReactiveModule.ceil`

`cross`

`cross(other: VectorSignal): VectorSignal`

Returns a vector signal with the value that is the cross product of the given signals.

**See Also**: `VectorSignal.dot`, `ScalarSignal.mul`, `VectorSignal.mul`

`delayBy`

`delayBy(timeSpan: {milliseconds: number}): this` Delays a signal. The argument is an object with a "milliseconds" property specifying the delay duration in milliseconds.

`distance`

`distance(other: PointSignal): ScalarSignal`

Returns the distance from the point to another point as a `ScalarSignal`.

`div`

`div(other: ScalarSignal): ScalarSignal`

Returns a signal with the value that is the value of the first signal divided by the value of the second signal.

**See Also**: `ReactiveModule.div`

`dot`

`dot(other: VectorSignal): ScalarSignal`

Returns a scalar signal with the value that is the dot product of the given signals.

**See Also**: `VectorSignal.cross`, `ScalarSignal.mul`, `VectorSignal.mul`

`expSmooth`

`expSmooth(dampFactor: number): PointSignal`

Smoothes a variable signal using exponential averaging over time. The argument specifies the dampening time constant in milliseconds.

**Note**: See also `ReactiveModule.expSmooth`.

`floor`

`floor(): ScalarSignal`

Returns a signal with the value that is the largest integer that is less than or equal to the value of the given signal.

**See Also**: `ReactiveModule.floor`

`fromRange`

`fromRange(x: ScalarSignal, min: ScalarSignal, max: ScalarSignal): ScalarSignal`

Maps x from \[min, max\] range to \[0.0, 1.0\] range.

`magnitude`

`magnitude(): ScalarSignal`

Returns the magnitude of the vector as a `ScalarSignal`.

`mod`

`mod(other: ScalarSignal): ScalarSignal`

Returns a signal with the value that is the floating-point remainder of the division of the value of the first signal by the value of the second signal.

**See Also**: `ReactiveModule.mod`

`mul`

`mul(other: ScalarSignal): ScalarSignal mul(other: VectorSignal): VectorSignal mul(other: ScalarSignal): VectorSignal mul(other: ScalarSignal): VectorSignal`

Returns a signal with the value that is the product of the values of the given signals.

**See Also**: `ReactiveModule.mul`, `ScalarSignal.mul`, `VectorSignal.mul`

`neg`

`neg(): ScalarSignal neg(): VectorSignal`

Returns a signal with the negated value of the given signal.

**See Also**: `ReactiveModule.neg`, `ScalarSignal.neg`, `VectorSignal.neg`

`normalize`

`normalize(v: VectorSignal): VectorSignal normalize(): VectorSignal`

Returns the normalized \(unit\) vector in the direction of the original vector as a `VectorSignal`.

`pow`

`pow(exponent: ScalarSignal): ScalarSignal`

Returns a signal with the value that is the base signal raised to the power of the exponent signal. The result is undefined if the base is negative, or if the base is zero and the exponent is not positive.

**See Also**: `ReactiveModule.pow`

`reflect`

`reflect(incident: VectorSignal, normal: VectorSignal): VectorSignal reflect(normal: VectorSignal): VectorSignal`

Calculates the reflection direction for an incident vector and a normal as a `VectorSignal`.

`round`

`round(): ScalarSignal`

Returns a signal with the value that is the rounded value of the given signal.

**Note**: When the fractional part is 0.5, it rounds the number away from zero, which is at odds with JavaScript standard behavior of rounding it always up in such cases. Therefore, this function is NOT exactly the reactive counterpart of the standard JavaScript `Math.round` utility.

**See Also**: `ReactiveModule.round`

`sign`

`sign(): ScalarSignal`

Returns a signal with the value that is the sign of the given signal. Possible sign values: NaN, -0.0, 0.0, -1.0, 1.0.

**Note**: this function is the reactive counterpart of the standard JavaScript `Math.sign` utility.

**See Also**: `ReactiveModule.sign`

`smoothStep`

`smoothStep(x: ScalarSignal, edge0: ScalarSignal, edge1: ScalarSignal): ScalarSignal`

Returns 0.0 if x is less than edge0, and 1.0 if x is greater than edge1. If x is between edge0 and edge1, smooth Hermite interpolation is performed.

`sqrt`

`sqrt(): ScalarSignal`

Returns a signal with the value that is the square root of the value of the given signal.

**See Also**: `ReactiveModule.sqrt`

`sub`

`sub(other: ScalarSignal): ScalarSignal sub(other: PointSignal): VectorSignal sub(other: VectorSignal): PointSignal sub(other: VectorSignal): VectorSignal`

Returns a signal with the value that is the difference of the values of the given signals.

**See Also**: `ReactiveModule.sub`, `ScalarSignal.sub`, `VectorSignal.sub`, `PointSignal.sub`

`sum`

`sum(other: ScalarSignal): ScalarSignal sum(other: VectorSignal): PointSignal sum(other: VectorSignal): VectorSignal sum(other: PointSignal): PointSignal`

Returns a signal with the value that is the sum of the values of the given signals.

**Note**: `add` and `sum` functions are synonyms, the behavior they provide is equivalent.

**See Also**: `ScalarSignal.sum`, ReactiveModule.add\`

`toRange`

`toRange(x: ScalarSignal, min: ScalarSignal, max: ScalarSignal): ScalarSignal`

Maps x from \[0.0, 1.0\] range to \[min, max\] range.

