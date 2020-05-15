# Picker

The `Picker` class describes an object controlling native picker behavior.

## **Example**

```text
//==============================================================================
// The following example demonstrates how to configure, show and use a NativeUI
// picker.
//
// Project setup:
// - Insert a plane
// - Create a material and assign it to the plane
// - Import textures for use in the picker (set these textures to uncompressed)
//==============================================================================

// Load in the required modules
const NativeUI = require('NativeUI');
const Scene = require('Scene');
const Textures = require('Textures');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

//==============================================================================
// Setup the configuration for the picker
//==============================================================================

// Locate the textures in the Assets
const texture0 = Textures.get('texture0');
const texture1 = Textures.get('texture1');
const texture2 = Textures.get('texture2');

// Store a reference to the picker
const picker = NativeUI.picker;

// Set a starting index (optional, will be 0 by default)
const index = 0;

// Create a configuration object
const configuration = {

  // The index of the selected item in the picker
  selectedIndex: index,

  // The image textures to use as the items in the picker
  items: [
    {image_texture: texture0},
    {image_texture: texture1},
    {image_texture: texture2},
    {image_texture: texture0},
    {image_texture: texture1},
    {image_texture: texture2},
    {image_texture: texture0},
    {image_texture: texture1},
    {image_texture: texture2}
  ]

};

//==============================================================================
// Apply the configuration and show the picker
//==============================================================================

// Configure the picker using the configuration object
picker.configure(configuration);

// Set the picker to be visible (visible is false by default)
picker.visible = true;

//==============================================================================
// Use the picker to set the texture of the plane
//==============================================================================

// Subscribe to the selectedIndex scalar signal
picker.selectedIndex.monitor().subscribe(function(index) {
  // Update the texture of the material assigned to the plane to be the selected
  // texture
  plane.material.diffuse = configuration.items[index.newValue].image_texture;
});
```

## **Properties** <a id="properties"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Property</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>selectedIndex</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) selectedIndex: ScalarSignal (set) selectedIndex: ScalarSignal</code>
        </p>
        <p>Represents the index of the selected item in the picker.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>visible</code>
      </td>
      <td style="text-align:left"><code>(set) visible: BoolSignal</code> Will instruct picker to be visible
        or not visible, according to passed boolean value.</td>
    </tr>
  </tbody>
</table>## **Methods** <a id="methods"></a>

| Method | Description |
| :--- | :--- |
| `configure` | `configure(configuration: {selectedIndex?: int, items: [{image_texture: ImageTexture}]}): void` Configures the picker with a given JSON configuration. The configuration consists of an optional initial selected index \(0 will be used if not specified\) and a list of items. For items you must specify a name of an uncompressed texture which will be used as the picker item image. |

