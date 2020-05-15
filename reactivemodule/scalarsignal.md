# ScalarSignal

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

`eq`

`eq(other: ScalarSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is **equal** to the value of the right-hand-side one, and the value of `false` all other time.

**Note**: the scalar values are tested for exact equality. For some applications it might be reasonable to perform a non-strict comparison allowing the values to be within a small distance one from another.

**See Also**: `ReactiveModule.eq`

`expSmooth`

`expSmooth(dampFactor: number): ScalarSignal`

Smoothes a variable signal using exponential averaging over time. The argument specifies the dampening time constant in milliseconds.

**Note**: See also `ReactiveModule.expSmooth`.

`floor`

`floor(): ScalarSignal`

Returns a signal with the value that is the largest integer that is less than or equal to the value of the given signal.

**See Also**: `ReactiveModule.floor`

`format`

`format(formatString: string): StringSignal`

Converts a `ScalarSignal` to a `StringSignal` according to the supplied formatting string.

**Note**: `formatString` shall conform to the Folly formatting rules as specified here: https://github.com/facebook/folly/blob/master/folly/docs/Format.md\#format-string-syntax .

**See Also**: `ScalarSignal.toString`.

`fromRange`

`fromRange(x: ScalarSignal, min: ScalarSignal, max: ScalarSignal): ScalarSignal`

Maps x from \[min, max\] range to \[0.0, 1.0\] range.

`ge`

`ge(other: ScalarSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is **greater than or equal** to the value of the right-hand-side one, and the value of `false` all other time.

**See Also**: `ReactiveModule.ge`

`gt`

`gt(other: ScalarSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is strictly **greater than** the value of the right-hand-side one, and the value of `false` all other time.

**See Also**: `ReactiveModule.gt`

`interval`

`interval(threshold: number): EventSource`

Returns an `EventSource` that emits an event whenever the supplied `ScalarSignal` first passes \(becomes greater than or equal\) a value of `N*threshold`, N = 1, 2, 3, ... Events are signaled in increasing order of N, starting from 1, with no omissions. For each value of N, the respective event is fired only once.

The emitted event \(the argument passed to the callback function\) has the value of corresponding `N*threshold`.

**Note**: The threshold must be a positive number.

**Note**: `interval` is mostly useful for non-negative non-decreasing scalar signals.

**See Also**: `ReactiveModule.trigger`, `ReactiveModule.multiTrigger`.

`le`

`le(other: ScalarSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is **less than or equal** to the value of the right-hand-side one, and the value of `false` all other time.

**See Also**: `ReactiveModule.le`

`lt`

`lt(other: ScalarSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is strictly **less than** the value of the right-hand-side one, and the value of `false` all other time.

**See Also**: `ReactiveModule.lt`

`magnitude`

`magnitude(): ScalarSignal`

Returns the magnitude of the vector as a `ScalarSignal`.

`mod`

`mod(other: ScalarSignal): ScalarSignal`

Returns a signal with the value that is the floating-point remainder of the division of the value of the first signal by the value of the second signal.

**See Also**: `ReactiveModule.mod`

`monitor`

`monitor(): EventSource monitor(config: { fireOnInitialValue: ?boolean}): EventSource`

Returns an `EventSource` that emits an event every time the value of the input signal changes. The event contains a JSON object with the old and new values in the format:

`{ "oldValue": val, "newValue": val }`

**Note**: By default, there is no event fired for the initial value of the signal. If `config.fireOnInitialValue` is set to `true` then an event for initial signal value is also emitted. `oldValue` is unset for this initial event.

`mul`

`mul(other: ScalarSignal): ScalarSignal mul(other: VectorSignal): VectorSignal mul(other: ScalarSignal): VectorSignal mul(other: ScalarSignal): VectorSignal`

Returns a signal with the value that is the product of the values of the given signals.

**See Also**: `ReactiveModule.mul`, `ScalarSignal.mul`, `VectorSignal.mul`

`multiTrigger`

`multiTrigger(threshold: number): EventSource`

Returns an `EventSource` that fires **every time** the signal raises to \(becomes greater than or equal after being less than\) the value of `threshold`.

The emitted event \(the argument passed to the callback function\) has the value of `threshold`.

**Note**: The initial value of the signal is assumed to be 0.0.

**See Also**: `ReactiveModule.trigger`, `ReactiveModule.interval`.

`ne`

`ne(other: ScalarSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is **not equal** to the value of the right-hand-side one, and the value of `false` all other time.

**Note**: the scalar values are tested for exact equality. For some applications it might be reasonable to perform a non-strict comparison allowing the values to be within a small distance one from another.

**See Also**: `ReactiveModule.ne`

`neg`

`neg(): ScalarSignal neg(): VectorSignal`

Returns a signal with the negated value of the given signal.

**See Also**: `ReactiveModule.neg`, `ScalarSignal.neg`, `VectorSignal.neg`

`normalize`

`normalize(v: VectorSignal): VectorSignal normalize(): VectorSignal`

Returns the normalized \(unit\) vector in the direction of the original vector as a `VectorSignal`.

`pin`

`pin(): ScalarSignal`

Returns a `ScalarSignal` containing a constant value which is the value of the specified signal immediately after `pin` is called.

`pinLastValue`

`pinLastValue(): ConstScalarSignal`

Returns a `ConstScalarSignal` containing a constant value which is the last value of the specified signal before `pinLastValue` is called. ConstScalarSignal can be passed to a functions which accept numbers.

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

`schmittTrigger`

`schmittTrigger(config: { low: number, high: number, initialValue: ?boolean}): BoolSignal`

Returns a Boolean signal that is `true` when the input is strictly greater than the upper threshold, and `false` when it is strictly less than the lower threshold. For input values between and including the thresholds, the Shmitt trigger returns the same value as at the previous update, or **initialValue** if this is the first update.

**Note**: The initialValue is assumed to be `false` if it isn't specified.

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

`toString`

`toString(): StringSignal`

Converts a `ScalarSignal` to a `StringSignal` according to the default string formatting rules.

**Note**: `ScalarSignal.format` allows more flexible control over the way the number is converted to string.

`trigger`

`trigger(threshold: number): EventSource`

Returns an `EventSource` that fires **the first time** the value of the signal raises \(becomes greater than or equal\) to the level of `threshold`. No more than one event is ever emitted by this `EventSource`.

The emitted event \(the argument passed to the callback function\) has the value of `threshold`.

**Note**: for positive thresholds, `trigger` is equivalent to `interval(threshold).take(1)`.

**See Also**: `ReactiveModule.multiTrigger`, `ReactiveModule.interval`.

