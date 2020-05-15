---
description: With v85 of Spark AR Studio the current JavaScript API will be deprecated in favor of asynchronous APIs.
---

# Asynchronous API Changes \(v85+\)

## Asynchronous API Changes \(v85+\) <a id="asynchronous-api-changes--v85--"></a>

With v85 of Spark AR Studio the current JavaScript API will be deprecated in favor of asynchronous APIs.

This means some APIs will be deprecated and will need to be replaced in your projects. When creating new projects, new APIs should be used instead.

### What happens to existing projects <a id="what-happens-to-existing-projects"></a>

APIs will be deprecated after 6 months in existing live effects, and 3 months in resubmitted projects.

If you’re using a deprecated API, you’ll:

1. See a message in Spark AR Studio when you open the project.
2. Get an email and notification to let you know how to update it.

## New APIs <a id="new-apis"></a>

## Deprecated `BlendShapesMesh`

**Note: duplicated functionality of Array&lt;BlendShapeMesh&gt;**

## `BlockSceneRoot`

**Added inputs.setBoolean\(name: String, signal: BoolSignal\): Promise&lt;void&gt;**

* Deprecates `setBooleanInput(name: String, signal: BoolSignal): void`

**Added inputs.setColor\(name: String, signal: ColorSignal\): Promise&lt;void&gt;**

* Deprecates `setColorInput(name: String, signal: ColorSignal): void`

**Added inputs.setPoint\(name: String, signal: PointSignal\): Promise&lt;void&gt;**

* Deprecates `setPointInput(name: String, signal: PointSignal): void`

**Added inputs.setPoint2D\(name: String, signal: PixelPointSignal\): Promise&lt;void&gt;**

* Deprecates `setPixelPointInput(name: String, signal: PixelPointSignal): void`

**Added inputs.setScalar\(name: String, signal: ScalarSignal\): Promise&lt;void&gt;**

* Deprecates `setScalarInput(name: String, signal: ScalarSignal): void`

**Added inputs.setShader\(name: String, signal: ShaderSignal\): Promise&lt;void&gt;**

* Deprecates `setShaderInput(name: String, signal: ShaderSignal): void`

**Added inputs.setString\(name: String, signal: StringSignal\): Promise&lt;void&gt;**

* Deprecates `setStringInput(name: String, signal: StringSignal): void`

**Added inputs.setVector\(name: String, signal: VectorSignal\): Promise&lt;void&gt;**

* Deprecates `setVectorInput(name: String, signal: VectorSignal): void`

**Added outputs.getBoolean\(name: String\): Promise&lt;BoolSignal&gt;**

* Deprecates `getBooleanOutput(name: String): BoolSignal`

**Added outputs.getBooleanOrFallback\(name: String, fallback: BoolSignal\): BoolSignal**

**Added outputs.getColor\(name: String\): Promise&lt;ColorSignal&gt;**

* Deprecates `getColorOutput(name: String): ColorSignal`

**Added outputs.getColorOrFallback\(name: String, fallback: ColorSignal\): ColorSignal**

**Added outputs.getPoint\(name: String\): Promise&lt;PointSignal&gt;**

* Deprecates `getPointOutput(name: String): PointSignal`

**Added outputs.getPointOrFallback\(name: String, fallback: PointSignal\): PointSignal**

**Added outputs.getPoint2D\(name: String\): Promise&lt;PixelPointSignal&gt;**

* Deprecates `getPixelPointOutput(name: String): PixelPointSignal`

**Added outputs.getPoint2DOrFallback\(name: String, fallback: PixelPointSignal\): PixelPointSignal**

**Added outputs.getScalar\(name: String\): Promise&lt;ScalarSignal&gt;**

* Deprecates `getScalarOutput(name: String): ScalarSignal`

**Added outputs.getScalarOrFallback\(name: String, fallback: ScalarSignal\): ScalarSignal**

**Added outputs.getShader\(name: String\): Promise&lt;ShaderSignal&gt;**

* Deprecates `getShaderOutput(name: String): ShaderSignal`

**Added outputs.getShaderOrFallback\(name: String, fallback: ShaderSignal\): ShaderSignal**

**Added outputs.getString\(name: String\): Promise&lt;StringSignal&gt;**

* Deprecates `getStringOutput(name: String): StringSignal`

**Added outputs.getStringOrFallback\(name: String, fallback: StringSignal\): StringSignal**

**Added outputs.getVector\(name: String\): Promise&lt;VectorSignal&gt;**

* Deprecates `getVectorOutput(name: String): VectorSignal`

**Added outputs.getVectorOrFallback\(name: String, fallback: VectorSignal\): VectorSignal**

## `Canvas`

**Added void setMode\(mode: Signal&lt;SceneModule.RenderMode&gt;, config { fallback: SceneModule.RenderMode }\): void**

**Added \(get\) mode: Signal&lt;SceneModule.RenderMode&gt;**

* Deprecates `(get) renderMode: SceneModule.RenderMode`

**Added \(set\) mode: Signal&lt;SceneModule.RenderMode&gt;**

* Deprecates `(set) renderMode: SceneModule.RenderMode`

## `CustomMaterial`

**Added getBoolParameter\(paramName: string\): Promise&lt;BoolSignal&gt;**

* Deprecates `boolParameter(paramName: string): BoolValue`

**Added getBoolParameterOrFallback\(paramName: string, fallback: BoolSignal\): BoolSignal**

**Added getFloatParameter\(paramName: string\): Promise&lt;ScalarSignal&gt;**

* Deprecates `floatParameter(paramName: string): ScalarValue`

#### Added `getFloatParameterOrFallback(paramName: string, fallback: ScalarSignal): ScalarSignal` <a id="added-getfloatparameterorfallback-paramname--string--fallback--scalarsignal---scalarsignal"></a>

**Added getTexture\(paramName: string\): Promise&lt;TextureBase&gt;**

**Added setBoolParameter\(paramName: string, source: BoolSignal\): Promise&lt;void&gt;**

* Deprecates `setBoolParameter(paramName: string, source: BoolSignal): void`

**Added setFloatParameter\(paramName: string, source: ScalarSignal\): Promise&lt;void&gt;**

* Deprecates `setFloatParameter(paramName: string, source: ScalarSignal): void`

**Added setTexture\(paramName: string, texture: TextureBase\): Promise&lt;void&gt;**

* Deprecates `setTexture(paramName: string, texture: TextureBase): void`

## `DefaultMaterial`

**Added getEmissive\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) emissive: TextureBase`

**Added getMultiply\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) multiply: TextureBase`

**Added getReflective\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) reflective: TextureBase`

## `DiagnosticsModule`

**Added typeSystem.getTypeDescriptions\(\): Promise&lt;Object&gt;**

* Deprecates `getTypeDescriptions(): Object`

**Added typeSystem.getModuleNames\(\): Promise&lt;Array&lt;string&gt;&gt;**

* Deprecates `getModuleNames(): Array<string>`

## `Face`

**Deprecated and marked for removal deformationCoefficientAt\(index: number\): ScalarSignal**

**Deprecated and marked for removal landmark2D\(index: number\): PointSignal**

#### `FaceMesh` <a id="facemesh"></a>

**Added getMaterial\(\): Promise&lt;MaterialBase&gt;**

* Deprecates `(get) material: MaterialBase`

## `FontsModule`

**Deprecated get\(fontName: string\): FontId**

* Use `findUsingPattern(namePattern: string, config: {limit: number}): Promise<Array<FontId>>` family of methods instead

## `InstructionModule`

**Added \(get\) automaticHintsEnabled: BoolSignal**

* Deprecates `(get) automaticInstructionsEnabled: boolean`

**Added \(set\) automaticHintsEnabled: BoolSignal**

* Deprecates `(set) automaticInstructionsEnabled: boolean`

## `LocaleModule`

**Deprecated \(get\) fromDevice: string**

* Use `(get) locale: StringSignal` instead

## `MaterialBase`

**Added getDiffuse\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) diffuse: TextureBase`

## `MaterialsModule`

**Deprecated get\(materialName: string\): MaterialBase**

* Use `findUsingPattern(namePattern: string, config: {limit: number}): Promise<Array<MaterialBase>>` family of methods instead

## `Mesh`

**Added getMaterial\(\): Promise&lt;MaterialBase&gt;**

* Deprecates `(get) material: MaterialBase`

**Deprecated \(get\) blendShapes: BlendShapesMesh**

* Use `getBlendShapes(): Promise<Array<BlendShape>>` instead

**Deprecated \(get\) materialIdentifier: String**

* Use `getMaterial(): Promise<MaterialBase>` instead

## `MetallicRoughnessPbrMaterial`

**Added getBaseColor\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) baseColor: TextureBase`

**Added getEmissive\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) emissive: TextureBase`

**Added getMetallicRoughness\(\): Promise&lt;TextureBase&gt;**

* Deprecates `(get) metallicRoughness: TextureBase`

## `ParticleSystem`

**Added getMaterial\(\): Promise&lt;MaterialBase&gt;**

* Deprecates `(get) material: MaterialBase`

**Added getTypes\(\): Promise&lt;Array&lt;ParticleTypeDescription&gt;&gt;**

* Deprecates `(get) types: Array<ParticleTypeDescription>`

**Added \(get\) innerRadius: ScalarSignal**

* Deprecates `(get) innerRadius: ScalarValue`

**Added \(get\) outerRadius: ScalarSignal**

* Deprecates `(get) outerRadius: ScalarValue`

#### Deprecated `ParticleTypeDescriptions` <a id="deprecated-particletypedescriptions"></a>

**Note: duplicated functionality of Array&lt;ParticleTypeDescription&gt;**

## `PatchesModule`

**Added inputs.setBoolean\(name: String, signal: BoolSignal\): Promise&lt;void&gt;**

* Deprecates `nsetBooleanValue(name: String, signal: BoolSignal): void`

**Added inputs.setColor\(name: String, signal: ColorSignal\): Promise&lt;void&gt;**

* Deprecates `setColorValue(name: String, signal: ColorSignal): void`

**Added inputs.setPoint\(name: String, signal: PointSignal\): Promise&lt;void&gt;**

* Deprecates `setPointValue(name: String, signal: PointSignal): void`

**Added inputs.setPoint2D\(name: String, signal: PixelPointSignal\): Promise&lt;void&gt;**

* Deprecates `setPoint2DValue(name: String, signal: PixelPointSignal): void`

**Added inputs.setPulse\(name: String, signal: EventSource\): Promise&lt;void&gt;**

* Deprecates `setPulseValue(name: String, signal: EventSource): void`

**Added inputs.setScalar\(name: String, signal: ScalarSignal\): Promise&lt;void&gt;**

* Deprecates `setScalarValue(name: String, signal: ScalarSignal): void`

**Added inputs.setString\(name: String, signal: StringSignal\): Promise&lt;void&gt;**

* Deprecates `setStringValue(name: String, signal: StringSignal): void`

**Added inputs.setVector\(name: String, signal: VectorSignal\): Promise&lt;void&gt;**

* Deprecates `setVectorValue(name: String, signal: VectorSignal): void`

**Added outputs.getBoolean\(name: String\): Promise&lt;BoolSignal&gt;**

* Deprecates `getBooleanValue(name: String): BoolSignal`

**Added outputs.getBooleanOrFallback\(name: String, fallback: BoolSignal\): BoolSignal**

**Added outputs.getColor\(name: String\): Promise&lt;ColorSignal&gt;**

* Deprecates `getColorValue(name: String): ColorSignal`

**Added outputs.getColorOrFallback\(name: String, fallback: ColorSignal\): ColorSignal**

**Added outputs.getPoint\(name: String\): Promise&lt;PointSignal&gt;**

* Deprecates `getPointValue(name: String): PointSignal`

**Added outputs.getPointOrFallback\(name: String, fallback: PointSignal\): PointSignal**

**Added outputs.getPoint2D\(name: String\): Promise&lt;PixelPointSignal&gt;**

* Deprecates `getPoint2DValue(name: String): PixelPointSignal`

**Added outputs.getPoint2DOrFallback\(name: String, fallback: PixelPointSignal\): PixelPointSignal**

**Added outputs.getPulse\(name: String\): Promise&lt;EventSource&gt;**

* Deprecates `getPulseValue(name: String): EventSource`

**Added outputs.getScalar\(name: String\): Promise&lt;ScalarSignal&gt;**

* Deprecates `getScalarValue(name: String): ScalarSignal`

**Added outputs.getScalarOrFallback\(name: String, fallback: ScalarSignal\): ScalarSignal**

**Added outputs.getString\(name: String\): Promise&lt;StringSignal&gt;**

* Deprecates `getStringValue(name: String): StringSignal`

**Added outputs.getStringOrFallback\(name: String, fallback: StringSignal\): StringSignal**

**Added outputs.getVector\(name: String\): Promise&lt;VectorSignal&gt;**

* Deprecates `getVectorValue(name: String): VectorSignal`

**Added outputs.getVectorOrFallback\(name: String, fallback: VectorSignal\): VectorSignal**

## `PlanarImage`

**Added getMaterial\(\): Promise&lt;MaterialBase&gt;**

* Deprecates `(get) material: MaterialBase`

#### `PlanarText` <a id="planartext"></a>

**Added getMaterial\(\): Promise&lt;MaterialBase&gt;**

* Deprecates `(get) material: MaterialBase`

## `Plane`

**Added getMaterial\(\): Promise&lt;MaterialBase&gt;**

* Deprecates `(get) material: MaterialBase`

#### `SceneObjectBase` <a id="sceneobjectbase"></a>

**Deprecated \(get\) materialIdentifier: string**

* Use `getMaterial(): Promise<MaterialBase>` on `SceneObjectBase` which support materials

**Deprecated find\(name: string\): SceneObjectBase**

* Use `findByPath(pathQuery: string, config: {limit: number}): Promise<Array<SceneObjectBase>>` family of methods instead

**Deprecated child\(name: string\): SceneObjectBase**

* Use `findByPath(pathQuery: string, config: {limit: number}): Promise<Array<SceneObjectBase>>` family of methods instead

## `Scene`

**Deprecated find\(name: string\): SceneObjectBase**

* Use `findByPath(pathQuery: string, config: {limit: number}): Promise<Array<SceneObjectBase>>` family of methods instead

**Deprecated child\(name: string\): SceneObjectBase**

* Use `findByPath(pathQuery: string, config: {limit: number}): Promise<Array<SceneObjectBase>>` family of methods instead

## `SvgImage`

**Added getSvg\(\): Promise&lt;Svg&gt;**

## `SvgsModule`

**Deprecated get\(svgName: string\): Svg**

* Use `findUsingPattern(namePattern: string, config: {limit: number}): Promise<Array<Svg>>` family of methods instead

## `TextAlignmentWrapper`

**Added \(get\) horizontal: Signal&lt;TextAlignment&gt;**

**Added \(set\) horizontal: Signal&lt;TextAlignment&gt;**

* Deprecates `(set) horizontal: TextAlignment`

**Added \(get\) vertical: Signal&lt;VerticalTextAlignment&gt;**

**Added \(set\) vertical: Signal&lt;VerticalTextAlignment&gt;**

* Deprecates `(set) vertical: VerticalTextAlignment`

## `TextExtrusion`

**Added getFrontMaterial\(\): Promise&lt;MaterialBase&gt;**

**Added getFont\(\): Promise&lt;FontId&gt;**

**Added getBackMaterial\(\): Promise&lt;MaterialBase&gt;**

**Added getSideMaterial\(\): Promise&lt;MaterialBase&gt;**

**Deprecated \(set\) faceMaterial: MaterialBase**

* Use `(set) frontMaterial: MaterialBase` and `(set) backMaterial: MaterialBase` instead

## `TexturesModule`

**Deprecated get\(textureName: string\): TextureBase**

* Use `findUsingPattern(namePattern: string, config: {limit: number}): Promise<Array<TextureBase>>` family of methods instead

  **Asynchronous API Changes \(v85+\)**

  With v85 of Spark AR Studio the current JavaScript API will be deprecated in favor of asynchronous APIs.

  This means some APIs will be deprecated and will need to be replaced in your projects. When creating new projects, new APIs should be used instead.

  **What happens to existing projects**

  APIs will be deprecated after 6 months in existing live effects, and 3 months in resubmitted projects.

  If you’re using a deprecated API, you’ll:

  1. See a message in Spark AR Studio when you open the project.
  2. Get an email and notification to let you know how to update it.

  \*\*\*\*

