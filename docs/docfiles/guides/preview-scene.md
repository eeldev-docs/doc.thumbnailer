---
sidebar_position: 3
description: Change the lighting, environment, floor and post processing of the Thumbnailer preview scene.
---

# Preview Scene

The **Scene** tab in the left panel changes the scene the asset is captured in. It uses the same preview scene settings as the Static Mesh and Skeletal Mesh editors.

| Setting | Description |
|---|---|
| **Profiles** | Save the scene settings as a profile and switch between profiles. Profiles are shared with the other asset editors. |
| **Lighting** | The intensity, color and direction of the directional light and the sky light. |
| **Environment** | The environment cube map, its rotation, and whether it is visible. Hide it to get a plain background. |
| **Floor** | Show or hide the floor. |
| **Post Processing** | Turn post processing on or off and change the post process settings, for example exposure and bloom. |

:::tip
For an even, flat look, hide the floor and the environment, and use a strong sky light. Turn on **Transparent** to remove the background completely. See [Transparent Thumbnails](/docfiles/guides/transparent-thumbnails).
:::

## Rendering settings during capture
Some rendering features make thumbnails look blurry or different from capture to capture. The **Rendering** settings under **Settings** turn them off while capturing, and most of them in the preview too:

- Anti-aliasing
- Auto exposure
- Motion blur
- Screen space reflections (also turns off screen space ambient occlusion in the preview)
- Eye adaptation

The console variables the plugin changes during a capture are restored as soon as the capture has finished. See [Settings](/docfiles/reference/settings#rendering).
