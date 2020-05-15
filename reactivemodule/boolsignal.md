# BoolSignal

`and`

`and(other: BoolSignal): BoolSignal`

Returns a signal with the value that is the logical conjunction of the values of the given signals. It is `true` every time both input signals are `true` and `false` at all other times.

**See Also**: `ReactiveModule.and`

`delayBy`

`delayBy(timeSpan: {milliseconds: number}): this` Delays a signal. The argument is an object with a "milliseconds" property specifying the delay duration in milliseconds.

`eq`

`eq(other: BoolSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is **equal** to the value of the right-hand-side one, and the value of `false` all other time.

**See Also**: `ReactiveModule.eq`

`ifThenElse`

`ifThenElse(thenValue: EventSource, elseValue: EventSource): EventSource ifThenElse(thenValue: ScalarSignal, elseValue: ScalarSignal): ScalarSignal ifThenElse(thenValue: StringSignal, elseValue: StringSignal): StringSignal ifThenElse(thenValue: BoolSignal, elseValue: BoolSignal): BoolSignal`

Returns a signal or an `EventSource` which at any point of time takes the value \(passes the events in case of `EventSource`\) of one or another inputs, depending on the momentary value of the given `BoolSignal`.

`monitor`

`monitor(): EventSource monitor(config: { fireOnInitialValue: ?boolean}): EventSource`

Returns an `EventSource` that emits an event every time the value of the input signal changes. The event contains a JSON object with the old and new values in the format:

`{ "oldValue": val, "newValue": val }`

**Note**: By default, there is no event fired for the initial value of the signal. If `config.fireOnInitialValue` is set to `true` then an event for initial signal value is also emitted. `oldValue` is unset for this initial event.

`ne`

`ne(other: BoolSignal): BoolSignal`

Returns a Boolean signal that takes the value of `true` every time when the value of the left-hand-side signal is **not equal** to the value of the right-hand-side one, and the value of `false` all other time.

**See Also**: `ReactiveModule.ne`

`not`

`not(): BoolSignal`

Returns a signal with the logically negated value of the given signal.

**See Also**: `ReactiveModule.not`

`onOff`

`onOff(): EventSource onOff(config: { fireOnInitialValue: ?boolean}): EventSource`

Returns an `EventSource` that emits an event every time the value of the input signal changes to `false`. The event contains a JSON object with the old and new values in the format:

`{ "oldValue": val, "newValue": val }`

**Note**: By default, there is no event fired for the initial value of the signal if it's `false` straight away. If `config.fireOnInitialValue` is set to `true` then an event for initial signal value is also emitted. `oldValue` is unset for this initial event.

`onOn`

`onOn(): EventSource onOn(config: { fireOnInitialValue: ?boolean}): EventSource`

Returns an `EventSource` that emits an event every time the value of the input signal changes to `true`. The event contains a JSON object with the old and new values in the format:

`{ "oldValue": val, "newValue": val }`

**Note**: By default, there is no event fired for the initial value of the signal if it's `true` straight away. If `config.fireOnInitialValue` is set to `true` then an event for initial signal value is also emitted. `oldValue` is unset for this initial event.

`or`

`or(other: BoolSignal): BoolSignal`

Returns a signal with the value that is the logical disjunction of the values of the given signals. It is `true` every time at least one of the input signals is `true` and `false` at all other times.

**See Also**: `ReactiveModule.or`

`pin`

`pin(): BoolSignal`

Returns a `BoolSignal` containing a constant value which is the value of the specified signal immediately after `pin` is called.

`pinLastValue`

`pinLastValue(): ConstBoolSignal`

Returns a `ConstBoolSignal` containing a constant value which is the last value of the specified signal before `pinLastValue` is called. ConstBoolSignal can be passed to a functions which accept bool.

`xor`

`xor(other: BoolSignal): BoolSignal`

Returns a signal with the value that is the logical exclusive disjunction of the values of the given signals. It is `true` every time exactly one of the input signals is `true` and `false` at all other times.

**Note**: It is equivalent to `BoolSignal.ne`.

**See Also**: `ReactiveModule.xor`

