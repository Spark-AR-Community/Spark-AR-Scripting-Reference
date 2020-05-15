# AnimationModule

The `AnimationModule` class implements object animation.

## Example

```text
//==============================================================================
// The following example demonstrates how to animate the properties of an object
// using drivers and samplers.
//
// Project setup:
// - Insert a plane
//==============================================================================

// Load in the required modules
const Animation = require('Animation');
const FaceTracking = require('FaceTracking');
const Scene = require('Scene');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

//==============================================================================
// Animate the plane's vertical scale according to mouth openness
//==============================================================================

// Store a reference to the mouth openness signal of a detected face
const mouthOpenness = FaceTracking.face(0).mouth.openness;

// Create a value driver using the mouth openness with the output normalized and
// clamped between 0.1 and 0.6
const mouthOpennessDriver = Animation.valueDriver(mouthOpenness, 0.1, 0.6);

// Create a sampler with a linear change from 1 to 2
const linearSampler = Animation.samplers.linear(1, 2);

// Create an animation combining the driver and sampler
const scaleAnimation = Animation.animate(mouthOpennessDriver, linearSampler);

// Bind the scale animation signal to the y-axis scale signal of the plane
plane.transform.scaleY = scaleAnimation;

//==============================================================================
// Animate the plane's horizontal position continuously
//==============================================================================

// Create a set of time driver parameters
const timeDriverParameters = {

  // The duration of the driver
  durationMilliseconds: 1500,

  // The number of iterations before the driver stops
  loopCount: Infinity,

  // Should the driver 'yoyo' back and forth
  mirror: true

};

// Create a time driver using the parameters
const timeDriver = Animation.timeDriver(timeDriverParameters);

// Create a sampler with a quadratic change in and out from -5 to 5
const quadraticSampler = Animation.samplers.easeInOutQuad(-5, 5);

// Create an animation combining the driver and sampler
const translationAnimation = Animation.animate(timeDriver, quadraticSampler);

// Bind the translation animation signal to the x-axis position signal of the plane
plane.transform.x = translationAnimation;

// Start the time driver (unlike value drivers this needs to be done explicitly)
timeDriver.start();
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
      <td style="text-align:left"><code>samplers</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) samplers: SamplerFactory (set) (Not Available)</code>
        </p>
        <p>Specifies an instance of a <code>SamplerFactory</code> object.</p>
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
      <td style="text-align:left"><code>animate</code>
      </td>
      <td style="text-align:left">
        <p><code>animate(driver: Driver, sampler: ScalarSampler): ScalarSignal animate(driver: Driver, sampler: ArrayOfScalarSamplers): ArrayOfScalarSignals animate(driver: Driver, sampler: RotationSampler): RotationSignal animate(driver: Driver, sampler: ColorSampler): RgbaSignal</code>
        </p>
        <p>Combines the driver and the sampler to create a signal that can be used
          to animate arbitrary properties of arbitrary objects.</p>
        <p>For <code>TimeDriver</code>-based animations the animation will start only
          when <code>TimeDriver.start</code> is invoked.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>timeDriver</code>
      </td>
      <td style="text-align:left">
        <p><code>timeDriver(timeDriverParams: {durationMilliseconds: number, loopCount: ?number, mirror: ?boolean}): TimeDriver</code>
        </p>
        <p>Returns a <code>TimeDriver</code> object that drives an animation for the
          specified parameters. <code>loopCount</code> defines the number of iterations
          before the time driver stops; this can be infinity. When <code>mirror</code> is <code>TRUE</code>,
          the time driver follows a <em>yoyo</em> effect with every odd iteration going
          forwards and every even iteration going backwards.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>valueDriver</code>
      </td>
      <td style="text-align:left">
        <p><code>valueDriver(value: ScalarSignal, min: number, max: number): ValueDriver</code>
        </p>
        <p>Returns a <code>ValueDriver</code> object that drives an animation based
          on values emitted from a <code>ScalarValue</code>. The signal values are
          normalized and clamped to maximum and minimum values.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`ArrayOfScalarSamplers`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.arrayofscalarsamplers) | The `ArrayOfScalarSamplers` class describes an array of scalar samplers. |
| [`ArrayOfScalarSignals`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.arrayofscalarsignals) | The `ArrayOfScalarSignals` class describes an array of scalar signals. |
| [`ColorSampler`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.colorsampler) | The `ColorSampler` class encapsulates a color sampler. |
| [`Driver`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.driver) | The `Driver` class encapsulates an animation driver. |
| [`RotationSampler`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.rotationsampler) | The `RotationSampler` class is an animation sampler for object rotation. |
| [`SamplerFactory`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.samplerfactory) | The `SamplerFactory` class creates different types of animation samplers. |
| [`ScalarSampler`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.scalarsampler) | The `ScalarSampler` class encapsulates a scalar value sampler. |
| [`SignalRecord`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.signalrecord) | The `SignalRecord` class encapsulates recording data for a value signal |
| [`SignalRecorder`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.signalrecorder) | The `SignalRecorder` class enables recording and playback of signal values |
| [`TimeDriver`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.timedriver) | The `TimeDriver` class controls an animation. |
| [`ValueDriver`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/animationmodule.valuedriver) | The `ValueDriver` class controls an animation value. |

