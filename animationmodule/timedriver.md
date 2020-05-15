# TimeDriver

The `TimeDriver` class controls an animation.

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
      <td style="text-align:left"><code>isRunning</code>
      </td>
      <td style="text-align:left">
        <p><code>isRunning(): BoolSignal</code>
        </p>
        <p>Returns a <code>BoolSignal</code> indicating whether the animation is running.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>onAfterIteration</code>
      </td>
      <td style="text-align:left">
        <p><code>onAfterIteration(): EventSource</code>
        </p>
        <p>Returns an <code>EventSource</code> to which you may subscribe. The event
          fires when the animation with loopCount completes an iteration. Subscribers
          will receive the one-based index of the completed iteration.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>onCompleted</code>
      </td>
      <td style="text-align:left">
        <p><code>onCompleted(): EventSource</code>
        </p>
        <p>Returns an <code>EventSource</code> to which you may subscribe. The event
          fires once when the animation completes.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>reset</code>
      </td>
      <td style="text-align:left">
        <p><code>reset(): void</code>
        </p>
        <p>Resets the driver progress to time point zero.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>reverse</code>
      </td>
      <td style="text-align:left">
        <p><code>reverse(): void</code>
        </p>
        <p>Reverses the animation from the moment it is called and goes back in time.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>start</code>
      </td>
      <td style="text-align:left">
        <p><code>start(): void</code>
        </p>
        <p>Starts the animation.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>stop</code>
      </td>
      <td style="text-align:left">
        <p><code>stop(): void</code>
        </p>
        <p>Stops or pauses the animation.</p>
      </td>
    </tr>
  </tbody>
</table>