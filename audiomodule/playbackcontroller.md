# PlaybackController

The `PlaybackController` class enables control of audio playback.

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
      <td style="text-align:left"><code>loop</code>
      </td>
      <td style="text-align:left">
        <p><code>loop(): void</code>
        </p>
        <p>Deprecated: Please use the <code>setLooping</code> method. Loop the playback
          controller, sound comes through all speakers (also known as Audio Source
          in the past) that reference the playback controller.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>play</code>
      </td>
      <td style="text-align:left">
        <p><code>play(): void</code>
        </p>
        <p>Deprecated: Please use the <code>setPlaying</code> method. Play the playback
          controller, sound comes through all speakers (also known as Audio Source
          in the past) that reference the playback controller.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>reset</code>
      </td>
      <td style="text-align:left">
        <p><code>reset(): void</code>
        </p>
        <p>Resets the playback controller audio to the beginning. If the playback
          controller is currently playing then it will immediately re-start.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>setLooping</code>
      </td>
      <td style="text-align:left">
        <p><code>setLooping(looping: BoolValue): void</code>
        </p>
        <p>Loops the playback controller. To be used in pair with the <code>setPlaying</code> method.
          If set to <code>true</code>, the audio will repeat infinitely.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>setPlaying</code>
      </td>
      <td style="text-align:left">
        <p><code>setPlaying(playing: BoolValue): void</code>
        </p>
        <p>Plays or pauses the playback controller depending on the value entered.
          When the audio is finished playing, use <code>reset</code> to play from the
          beginning.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>stop</code>
      </td>
      <td style="text-align:left"><code>stop(): void</code> Deprecated: Please use the <code>setPlaying</code> method
        to pause the audio or the <code>reset</code> method to return the audio to
        the beginning. Stop the playback controller.</td>
    </tr>
  </tbody>
</table>