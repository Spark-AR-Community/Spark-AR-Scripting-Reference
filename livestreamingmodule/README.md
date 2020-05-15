# LiveStreamingModule

The `LiveStreamingModule` class enables to retrieve information from a live stream from within the effect, such as reactions and comments.

## Example

```text
//==============================================================================
// The following example demonstrates how to dynamically update an effect based
// on the reactions and comments of a viewer during a livestream.
//
// Project setup:
// - Insert two text objects
//==============================================================================

// Load in the required modules
const LiveStreaming = require('LiveStreaming');
const Scene = require('Scene');

// Locate the text objects in the Scene
const angryCountText = Scene.root.find('text0');
const matchCounterText = Scene.root.find('text1');

// Store references to the reactions and comments properties
const reactions = LiveStreaming.reactions;
const comments = LiveStreaming.comments;

//==============================================================================
// Displaying a number based on the number of a certain reaction from viewers
//==============================================================================

// Store a reference to the number of angry reactions
const angryCount = reactions.angry;

// Bind the number of angry reactions to the text object
angryCountText.text = angryCount.toString();

//==============================================================================
// Displaying a string based on the number of comments from viewers
//==============================================================================

// Define what strings we want to start a counter for
const matchStrings = ['cat','dog'];

// Define if those strings should be case sensitive or not
const isCaseSensitive = false;

// Create a variable to store the highest count
var leadingCount = 0;

// Subscribe to the startMatchCounter EventSource
comments.startMatchCounter(matchStrings,isCaseSensitive).subscribe(
function(result) {

    // Loop through the keys in the result (e.g. 'cat' or 'dog')
    for (var key in result) {

        // Update the text and leadingCount if the count of the result is
        // is greater than the current leadingCount
        if (result[key] > leadingCount) {
            matchCounterText.text = key;
            leadingCount = result[key];
        }

    }

});
```

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
      <td style="text-align:left"><code>comments</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) comments: LiveStreamingComments (set) (Not Available)</code>
        </p>
        <p>Provides access to a <code>LiveStreamingComments</code> object that encapsulates
          data about the live stream&apos;s comments.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>concurrentViewerCount</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) concurrentViewerCount: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Provides access to a <code>ScalarSignal</code> that encapsulates the number
          of concurrent viewers of the live stream.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>reactions</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) reactions: LiveStreamingReactions (set) (Not Available)</code>
        </p>
        <p>Provides access to a <code>LiveStreamingReactions</code> object that encapsulates
          data about the live stream&apos;s reactions.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>state</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) state: LiveStreaming.State (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>LiveStreaming.State</code> enum value indicating the broadcast
          state.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

| Class | Description |
| :--- | :--- |
| [`LiveStreamingComments`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/livestreamingmodule.livestreamingcomments) | The `LiveStreamingComments` class provides access to the Facebook Live comments stream. |
| [`LiveStreamingReactions`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/livestreamingmodule.livestreamingreactions) | The `LiveStreamingReactions` class provides access to the Facebook Live reactions stream. For low volumes of reactions this will correspond to the stream of reaction bubbles that float by the broadcast, for higher volumes of reactions this will an approximate count of how many times the reaction button was tapped, with some rate limiting per-user. This number will not correspond to the number of reactions displayed elsewhere because that number only counts each user's reaction once. |

## Enums

| Enum | Description |
| :--- | :--- |
| [`State`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/livestreamingmodule.state) | The `LiveStreamingModule.State` enum describes the state of a live stream. |

