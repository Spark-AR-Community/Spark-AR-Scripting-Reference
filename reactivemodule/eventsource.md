# EventSource

The `EventSource` class provides methods for monitoring signals.

## Properties

This module exposes no properties.

## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>select</code>
      </td>
      <td style="text-align:left">
        <p><code>select(property: string): EventSource</code>
        </p>
        <p>Converts event source by selecting a property in the event object. Events
          without specified property are ignored.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>skip</code>
      </td>
      <td style="text-align:left">
        <p><code>skip(count: number): EventSource</code>
        </p>
        <p>Yields a filtered event source: the first <code>count</code> events from
          the original source are dropped, and subsequent ones signaled.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>subscribe</code>
      </td>
      <td style="text-align:left">
        <p><code>subscribe(callback: (event: mixed) =&gt; void): Subscription</code>
        </p>
        <p>Sets a callback for the event source. The callback will be invoked every
          time an event is emitted from this <code>EventSource</code>.</p>
        <p><b>See Also</b>: <code>Subscription.unsubscribe</code>.</p>
        <p><b>Note</b>: <code>subscribe</code> and <code>subscribeOnNext</code> functions
          are completely equivalent.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>subscribeOnNext</code>
      </td>
      <td style="text-align:left">
        <p><code>subscribeOnNext(callback: (event: mixed) =&gt; void): Subscription</code>
        </p>
        <p>Sets a callback for the event source. The callback will be invoked every
          time an event is emitted from this <code>EventSource</code>.</p>
        <p><b>See Also</b>: <code>Subscription.unsubscribe</code>.</p>
        <p><b>Note</b>: <code>subscribe</code> and <code>subscribeOnNext</code> functions
          are completely equivalent.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>subscribeWithSnapshot</code>
      </td>
      <td style="text-align:left">
        <p><code>subscribeWithSnapshot(snapshot: { [name: string]: Signal}, callback: (event: mixed, snapshot: mixed) =&gt; void): Subscription</code>
        </p>
        <p>Sets a callback for the event source, similar to <code>Subscribe</code> function,
          but with additional <code>Snapshot</code> parameter. <code>Snapshot</code> is
          a dictionary of String/Bool/Scalar signals, which will be passed as JSON
          to the callback function using lastValue from requested signals</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>take</code>
      </td>
      <td style="text-align:left">
        <p><code>take(count: number): EventSource</code>
        </p>
        <p>Yields a filtered event source: the first <code>count</code> events from
          the original source are signaled, and subsequent ones ignored.</p>
      </td>
    </tr>
  </tbody>
</table>