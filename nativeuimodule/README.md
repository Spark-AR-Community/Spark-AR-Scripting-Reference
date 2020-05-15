# NativeUIModule

The `NativeUI` module exposes editable text.

## Example

```text
//==============================================================================
// The following example demonstrates how to get and set the value of editable
// text through scripting and keyboard input.
//
// Project setup:
// - Insert text
// - Set the text to 'Editable' in the inspector
// - Add the 'Editable text' capability under 'Native UI Control'
// - Add the 'Tap Gesture' capability under 'Touch Gestures'
//==============================================================================

// Load in the required modules
const Diagnostics = require('Diagnostics');
const NativeUI = require('NativeUI');
const TouchGestures = require('TouchGestures');

// Set the initial text value
NativeUI.setText('text0','Default Text');

// Subscribe to tap gestures
TouchGestures.onTap().subscribe(function () {

  // Enter text editing mode
  NativeUI.enterTextEditMode('text0');

});

// Subscribe to changes in the text
NativeUI.getText('text0').monitor().subscribe(function(textUpdate){

  // Log the new text value to the console
  Diagnostics.log('You entered ' + textUpdate.newValue);

});
```

## Properties

| Property | Description |
| :--- | :--- |
| `picker` | `(get) picker: Picker (set) picker: Picker` Represents the picker object. |
| `slider` | `(get) slider: Slider (set) slider: Slider` Represents the slider object. |

## Methods

| Method | Description |
| :--- | :--- |
| `enterTextEditMode` | `enterTextEditMode(nodeName: String): void` Requests user input for given node. |
| `getText` | `getText(nodeName: String): StringSignal` Gets the user edited text of the given node. |
| `setText` | `setText(nodeName: String, text: String): void` Sets the text to the provided value for the node with a given name. |

## Classes

| Class | Description |
| :--- | :--- |
| [`Picker`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/nativeuimodule.picker) | The `Picker` class describes an object controlling native picker behavior. |
| [`Slider`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/nativeuimodule.slider) | The `Slider` class describes an object controlling native slider behavior. |

