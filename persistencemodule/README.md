# PersistenceModule

The `Persistence` class encapsulates persistent objects.

## Example

```text
//==============================================================================
// The following example demonstrates how to store, retrieve and remove data
// across multiple sessions.
//
// Project setup:
// - Insert two rectangles
// - Insert text
// - Position the rectangles and text so that all are visible
// - Add 'data' to 'Whitelisted keys' under the 'Persistence' Capability
// - Add the 'Tap Gesture' capability under 'Touch Gestures'
//==============================================================================

// Load in the required modules
const Persistence = require('Persistence');
const Scene = require('Scene');
const TouchGestures = require('TouchGestures');

// Locate the rectangles and text in the Scene
const storeRectangle = Scene.root.find('rectangle0');
const removeRectangle = Scene.root.find('rectangle1');
const dataText = Scene.root.find('text0');

// Store a reference to the userScope
const userScope = Persistence.userScope;

// Create a JavaScript object to store the data
const data = { name: 'Spark AR' };

//==============================================================================
// How to get stored data
//==============================================================================

// Attempt to get the stored data and if successful...
userScope.get('data').then(function(result) {

  // Output a success message with the data added
  dataText.text = 'Successfully retrieved data ' + result.name;

// If not successful...
}).catch(function(error) {

  // Output a failure message with the error returned
  dataText.text = 'Failed to retrieve data, ' + error;

});

//==============================================================================
// How to store data
//==============================================================================

// Subscribe to tap gestures on the storeRectangle
TouchGestures.onTap(storeRectangle).subscribe(function() {

  // Attempt to store the data and if successful...
  userScope.set('data',data).then(function(result) {

    // Output a success message
    dataText.text = 'Successfully stored';

  // If not successful...
  }).catch(function(error) {

    // Output a failure message with the error returned
    dataText.text = 'Failed to store, ' + error;

  });

});

//==============================================================================
// How to remove stored data
//==============================================================================

// Subscribe to tap gestures on the removeRectangle
TouchGestures.onTap(removeRectangle).subscribe(function() {

  // Attempt to remove the data and if successful...
  userScope.remove('data').then(function(result) {

    // Output a success message
    dataText.text = 'Successfully removed';

  // If not successful...
  }).catch(function(error) {

    // Output a failure message with the error returned
    dataText.text = 'Failed to remove, ' + error;

  });

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
      <td style="text-align:left"><code>userScope</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) userScope: StorageScope</code>
        </p>
        <p>Gets an instance of StorageScope corresponding to the user scope</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

| Class | Description |
| :--- | :--- |
| [`StorageScope`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/persistencemodule.storagescope) | The `StorageScope` class encapsulates different methods of storage for persistent objects. |

