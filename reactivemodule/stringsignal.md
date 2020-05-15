# StringSignal

The `StringSignal` class monitors a string value.

## Properties

<table>
  <thead>
    <tr>
      <th style="text-align:left">Property</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>lastValue</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) lastValue: string (set) (Not Available)</code>
        </p>
        <p>Specifies a string that represents the last value of the signal.</p>
        <p><b>Note</b>: The signal value is updated during simulation tick. This
          means that the value of <code>lastValue</code> is undefined before its first
          update. It is also undefined for signals that aren&apos;t used for any
          bindings/subscriptions, because those signals aren&apos;t guaranteed to
          be updated at each simulation tick.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>concat</code>
      </td>
      <td style="text-align:left">
        <p><code>concat(other: StringSignal): StringSignal</code>
        </p>
        <p>Returns a <code>StringSignal</code> containing the concatenation of the
          values specified by the input signals.</p>
        <p><b>See Also</b>: <code>ReactiveModule.concat</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>delayBy</code>
      </td>
      <td style="text-align:left"><code>delayBy(timeSpan: {milliseconds: number}): this</code> Delays a signal.
        The argument is an object with a &quot;milliseconds&quot; property specifying
        the delay duration in milliseconds.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>eq</code>
      </td>
      <td style="text-align:left">
        <p><code>eq(other: StringSignal): BoolSignal</code>
        </p>
        <p>Returns a Boolean signal that takes the value of <code>true</code> every
          time when the value of the left-hand-side signal is <b>equal</b> to the value
          of the right-hand-side one, and the value of <code>false</code> all other
          time.</p>
        <p><b>See Also</b>: <code>ReactiveModule.eq</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>monitor</code>
      </td>
      <td style="text-align:left">
        <p><code>monitor(): EventSource monitor(config: { fireOnInitialValue: ?boolean}): EventSource</code>
        </p>
        <p>Returns an <code>EventSource</code> that emits an event every time the value
          of the input signal changes. The event contains a JSON object with the
          old and new values in the format:</p>
        <p><code>{ &quot;oldValue&quot;: val, &quot;newValue&quot;: val }</code>
        </p>
        <p><b>Note</b>: By default, there is no event fired for the initial value
          of the signal. If <code>config.fireOnInitialValue</code> is set to <code>true</code> then
          an event for initial signal value is also emitted. <code>oldValue</code> is
          unset for this initial event.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>ne</code>
      </td>
      <td style="text-align:left">
        <p><code>ne(other: StringSignal): BoolSignal</code>
        </p>
        <p>Returns a Boolean signal that takes the value of <code>true</code> every
          time when the value of the left-hand-side signal is <b>not equal</b> to the
          value of the right-hand-side one, and the value of <code>false</code> all
          other time.</p>
        <p><b>See Also</b>: <code>ReactiveModule.ne</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>pin</code>
      </td>
      <td style="text-align:left">
        <p><code>pin(): StringSignal</code>
        </p>
        <p>Returns a <code>StringSignal</code> containing a constant value which is
          the value of the specified signal immediately after <code>pin</code> is called.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>pinLastValue</code>
      </td>
      <td style="text-align:left">
        <p><code>pinLastValue(): ConstStringSignal</code>
        </p>
        <p>Returns a <code>ConstStringSignal</code> containing a constant value which
          is the last value of the specified signal before <code>pinLastValue</code> is
          called. ConstStringSignal can be passed to a functions which accept strings</p>
      </td>
    </tr>
  </tbody>
</table>