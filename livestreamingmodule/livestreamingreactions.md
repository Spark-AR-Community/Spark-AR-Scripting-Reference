# LiveStreamingReactions

The `LiveStreamingReactions` class provides access to the Facebook Live reactions stream. For low volumes of reactions this will correspond to the stream of reaction bubbles that float by the broadcast, for higher volumes of reactions this will an approximate count of how many times the reaction button was tapped, with some rate limiting per-user. This number will not correspond to the number of reactions displayed elsewhere because that number only counts each user's reaction once.

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
      <td style="text-align:left"><code>angry</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) angry: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the count of the angry reaction
          for this live stream.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>haha</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) haha: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the count of the haha reaction
          for this live stream.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>like</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) like: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the count of the like reaction
          for this live stream.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>love</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) love: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the count of the love reaction
          for this live stream.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sad</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) sad: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the count of the sad reaction
          for this live stream.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>total</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) total: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the total number of reactions
          on this live stream. This may exceed the sum of the individual reaction
          counts (like, love, etc.) if a seasonal reaction (such as thankful) is
          available and is used by viewers.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>wow</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) wow: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> that is the count of the wow reaction
          for this live stream.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

