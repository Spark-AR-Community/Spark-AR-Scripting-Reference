---
description: The SamplerFactory class creates different types of animation samplers.
---

# SamplerFactory

`bezier`

`bezier(p0: number, p1: number, p2: number, p3: number): ScalarSampler bezier(p0: Array<number>, p1: Array<number>, p2: Array<number>, p3: Array<number>): ArrayOfScalarSamplers`

Returns a sampler object that generates values of a cubic Bezier curve with the specified control points. The control points are assumed to be equidistant along the parameter axis.

`constant`

`constant(value: number): ScalarSampler constant(value: Array<number>): ArrayOfScalarSamplers`

Returns a sampler that returns the same value at all points in the animation.

`easeInBack`

`easeInBack(beginValue: number, endValue: number): ScalarSampler easeInBack(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInBounce`

`easeInBounce(beginValue: number, endValue: number): ScalarSampler easeInBounce(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInCirc`

`easeInCirc(beginValue: number, endValue: number): ScalarSampler easeInCirc(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInCubic`

`easeInCubic(beginValue: number, endValue: number): ScalarSampler easeInCubic(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInElastic`

`easeInElastic(beginValue: number, endValue: number): ScalarSampler easeInElastic(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInExpo`

`easeInExpo(beginValue: number, endValue: number): ScalarSampler easeInExpo(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutBack`

`easeInOutBack(beginValue: number, endValue: number): ScalarSampler easeInOutBack(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutBounce`

`easeInOutBounce(beginValue: number, endValue: number): ScalarSampler easeInOutBounce(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutCirc`

`easeInOutCirc(beginValue: number, endValue: number): ScalarSampler easeInOutCirc(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutCubic`

`easeInOutCubic(beginValue: number, endValue: number): ScalarSampler easeInOutCubic(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutElastic`

`easeInOutElastic(beginValue: number, endValue: number): ScalarSampler easeInOutElastic(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutExpo`

`easeInOutExpo(beginValue: number, endValue: number): ScalarSampler easeInOutExpo(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutQuad`

`easeInOutQuad(beginValue: number, endValue: number): ScalarSampler easeInOutQuad(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutQuart`

`easeInOutQuart(beginValue: number, endValue: number): ScalarSampler easeInOutQuart(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutQuint`

`easeInOutQuint(beginValue: number, endValue: number): ScalarSampler easeInOutQuint(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInOutSine`

`easeInOutSine(beginValue: number, endValue: number): ScalarSampler easeInOutSine(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInQuad`

`easeInQuad(beginValue: number, endValue: number): ScalarSampler easeInQuad(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInQuart`

`easeInQuart(beginValue: number, endValue: number): ScalarSampler easeInQuart(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInQuint`

`easeInQuint(beginValue: number, endValue: number): ScalarSampler easeInQuint(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeInSine`

`easeInSine(beginValue: number, endValue: number): ScalarSampler easeInSine(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutBack`

`easeOutBack(beginValue: number, endValue: number): ScalarSampler easeOutBack(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutBounce`

`easeOutBounce(beginValue: number, endValue: number): ScalarSampler easeOutBounce(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutCirc`

`easeOutCirc(beginValue: number, endValue: number): ScalarSampler easeOutCirc(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutCubic`

`easeOutCubic(beginValue: number, endValue: number): ScalarSampler easeOutCubic(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutElastic`

`easeOutElastic(beginValue: number, endValue: number): ScalarSampler easeOutElastic(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutExpo`

`easeOutExpo(beginValue: number, endValue: number): ScalarSampler easeOutExpo(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutQuad`

`easeOutQuad(beginValue: number, endValue: number): ScalarSampler easeOutQuad(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutQuart`

`easeOutQuart(beginValue: number, endValue: number): ScalarSampler easeOutQuart(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutQuint`

`easeOutQuint(beginValue: number, endValue: number): ScalarSampler easeOutQuint(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`easeOutSine`

`easeOutSine(beginValue: number, endValue: number): ScalarSampler easeOutSine(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Easing sampler. Behaves similarly to the linear sampler, but with easing functions at the beginning and/or end.

`frame`

`frame(numberOfFrames: number): ScalarSampler frame(numberOfFrames: number, startFrame: number): ScalarSampler frame(numberOfFrames: Array<number>): ArrayOfScalarSamplers frame(numberOfFrames: Array<number>, startFrame: Array<number>): ArrayOfScalarSamplers`

Returns a sampler object that cyclically generates integer frame numbers in the range \[0..`numberOfFrames`-1\] as the attached driver's progress goes from 0.0 to 1.0.

If the `startFrame` is supplied, then the output values are shifted by that value.

`HSVA`

`HSVA(channelSamplers: ArrayOfScalarSamplers): ColorSampler`

Returns a sampler that specifies a color by interpreting the provided samplers as HSVA channels, respectively.

The dimension of `channelSamplers` must be exactly 4. `channelSamplers` must be an instance of `ArrayOfScalarSamplers`, not a regular JS Array object.

`linear`

`linear(beginValue: number, endValue: number): ScalarSampler linear(beginValue: Array<number>, endValue: Array<number>): ArrayOfScalarSamplers`

Returns a sampler object that generates values that change linearly from `beginValue` to `endValue` as the attached driver's progress goes from 0.0 to 1.0.

`polybezier`

`polybezier(config: { keyframes: Array<number>, knots: ?Array<number>, tangents: ?Array<number> }): ScalarSampler polybezier(config: { keyframes: Array<Array<number>>, knots: ?Array<number>, tangents: ?Array<Array<number>> }): ArrayOfScalarSamplers`

Returns a sampler object that generates values of a piecewise cubic Bezier spline that goes through specified `keyframes` as the attached driver's progress goes from 0.0 to 1.0 through normalized `knots` points.

When `tangents` is specified, the curve is C1-smooth, otherwise the curve is C2-smooth and the second derivatives at the begin and end points are zero.

The dimensions of `config.keyframes` and `config.knots`, if specified, and `config.tangents`, if specified, arrays must be equal and have no less than 2 elements. The first element of `config.knots`, if specified, must always be zero. If `config.knots` is not specified then the knot sequence is defaulted to \[0, 1, 2, ..., `config.keyframes.length` - 1\].

`polyline`

`polyline(config: { keyframes: Array<number>, knots: ?Array<number> }): ScalarSampler polyline(config: { keyframes: Array<Array<number>>, knots: ?Array<number> }): ArrayOfScalarSamplers polyline(config: { keyframes: Array<Rotation>, knots: ?Array<number> }): RotationSampler`

Returns a sampler object that generates values that goes piecewise linearly through specified `keyframes` as the attached driver's progress goes from 0.0 to 1.0 through normalized `knots` points.

The dimensions of the `config.keyframes` and `config.knots` arrays, if specified, must be equal and be not less than 2. The first element of `config.knots`, if specified, must be zero. If `config.knots` is not specified then the knot sequence defaults to \[0, 1, 2, ..., `config.keyframes.length` - 1\].

`RGBA`

`RGBA(channelSamplers: ArrayOfScalarSamplers): ColorSampler`

Returns a sampler that specifies a color by interpreting the provided samplers as RGBA channels, respectively.

The dimension of `channelSamplers` must be exactly 4. `channelSamplers` must be an instance of `ArrayOfScalarSamplers`, not a JavaScript Array object.

`sequence`

`sequence(config: { samplers: Array<ScalarSampler>, knots: ?Array<number> }): ScalarSampler sequence(config: { samplers: Array<ArrayOfScalarSamplers>, knots: ?Array<number> }): ArrayOfScalarSamplers`

Returns an animation sequence built from provided segments with respect to the optionally provided knots.

`config.samplers` must contain at least 2 elements. `config.knots`, if specified, must contain exactly `config.samplers.length`+1 elements. The first element of `config.knots`, when specified, must always be zero. If `config.knots` is not specified then the knot sequence defaults to \[0, 1, 2, ..., `config.samplers.length`\].

