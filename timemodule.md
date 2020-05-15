# TimeModule

`clearInterval`

`clearInterval(timer: Subscription): void`

Cancels a callback set by `setInterval`. This function is provided as a to match the traditional JS `clearInterval` API.

**Note**: This is equivalent to `Subscription.unsubscribe`.

`clearTimeout`

`clearTimeout(timer: Subscription): void`

Cancels a callback set by `setTimeout`. This has no effect if the timeout has already been triggered. This function is provided as a to match the traditional JS `clearTimeout` API.

**Note**: This is equivalent to `Subscription.unsubscribe`.

`setInterval`

`setInterval(callback: Function, delay: Number): Subscription`

Returns a `Subscription` object. The function specified by `callback` is called at intervals specified by `delay` in milliseconds. The `setInterval` will continue calling the `callback` until `TimeModule.clearInterval` is called. The `callback` is a function that has one argument, the elapsed time since the timer started. An exception is thrown when the `delay` is zero or less.

**Note**: An interval can be canceled either via `Subscription.unsubscribe` or `TimeModule.clearInterval`.

`setIntervalWithSnapshot`

`setIntervalWithSnapshot(snapshot: { [name: string]: Signal}, callback: Function, delay: Number): Subscription` Returns a `Subscription` object. The function specified by `callback` is called at intervals specified by `delay` in milliseconds using `Snapshot` of signals. `Snapshot` is a dictionary of String/Bool/Scalar signals, which will be passed as JSON to the callback function using lastValue from requested signals.

The `setIntervalWithSnapshot` will continue calling the `callback` until `TimeModule.clearInterval` is called. The `callback` is a function that has two arguments, the elapsed time since the timer started, and the snapshot JSON An exception is thrown when the `delay` is zero or less.

**Note**: An interval can be canceled either via `Subscription.unsubscribe` or `TimeModule.clearInterval`.

`setTimeout`

`setTimeout(callback: Function, delay: Number): Subscription`

Returns a `Subscription` object. The function specified by `callback` is called after the specified `delay` in milliseconds. The `callback` is a function that has one argument, the elapsed time since the timer started.

**Note**: A timeout can be canceled either via `Subscription.unsubscribe` or `TimeModule.clearTimeout`.

**Note**: This is equivalent to `Time.ms.sub(Time.ms.pin()).trigger(delay).subscribe(callback)`.

`setTimeoutWithSnapshot`

`setTimeoutWithSnapshot(snapshot: { [name: string]: Signal}, callback: Function, delay: Number): Subscription`

Returns a `Subscription` object. The function specified by `callback` is called after the specified `delay` in milliseconds using `Snapshot` of signals. `Snapshot` is a dictionary of String/Bool/Scalar signals, which will be passed as JSON to the callback function using lastValue from requested signals.

The `callback` is a function that has two arguments, the elapsed time since the timer started and the snapshot JSON.

**Note**: A timeout can be canceled either via `Subscription.unsubscribe` or `TimeModule.clearTimeout`.

**Note**: This is equivalent to `Time.ms.sub(Time.ms.pin()).trigger(delay).subscribeWithSnapshot(snapshot, callback)`.

