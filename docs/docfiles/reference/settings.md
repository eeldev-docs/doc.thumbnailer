---
sidebar_position: 1
description: Every setting of the Thumbnailer plugin, with defaults.
---

# Settings

The settings are on the **Settings** tab in the Thumbnailer window, and in **Edit → Editor Preferences → Plugins → Thumbnailer**. Both show the same settings.

The settings are saved per user and per project in `Saved/Config/<Platform>Editor/EditorPerProjectUserSettings.ini`, under `[/Script/Thumbnailer.ThumbnailerSettings]`. They are not shared through source control. The camera bookmarks and the default view are saved there too.

## Camera
| Setting | Default | Description |
|---|---|---|
| Camera Type | `Perspective` | `Perspective` or `Orthographic`. See [Camera and Framing](/docfiles/guides/camera#perspective-or-orthographic). |
| Field of View (FOV) | `85` | The field of view of the perspective camera. A smaller value gives a flatter look. Only used with `Perspective`. |

## Output
| Setting | Default | Description |
|---|---|---|
| Thumbnail Resolution | `512 x 512` | The width and height of the thumbnail. Also set under **Output** in the right panel. |
| File Extension | `PNG` | `PNG` or `TGA`. Also set under **Output** in the right panel. |
| Save Dir | `Thumbnails` | The folder in Content the thumbnails are imported to. `Thumbnails` is `/Game/Thumbnails`. |
| File Prefix | `Thumb_` | Added before the asset name, for example `Thumb_SM_Chair`. |
| Override Thumbnail Name | Empty | Replaces the asset name in the file name. Not saved, it is cleared when the editor restarts. |
| Transparent Thumbnail | Off | Removes the background when capturing. See [Transparent Thumbnails](/docfiles/guides/transparent-thumbnails). |
| Hide Editor Billboards | On | Hides the editor billboards (sprites) of an actor, for example the icons of lights and audio components. |

An empty **Save Dir** or **File Prefix** is set back to its default.

## Rendering
These features are turned off while capturing, and most of them in the preview too. The console variables are changed only during the capture and are restored afterwards.

| Setting | Default | Description |
|---|---|---|
| Disable Anti Aliasing | On | Turns off anti-aliasing and temporal anti-aliasing. |
| Disable Auto Exposure | On | Turns off auto exposure (`r.DefaultFeature.AutoExposure`). |
| Disable Motion Blur | On | Turns off motion blur (`r.DefaultFeature.MotionBlur`, `r.MotionBlurQuality`). |
| Disable Screen Space Reflections | On | Turns off screen space reflections (`r.SSR.Quality`). Also turns off screen space ambient occlusion in the preview. |
| Disable Eye Adaption | Off | Turns off eye adaptation (`r.EyeAdaptationQuality`). |

## Viewport
These settings only change the preview. Nothing here is part of the capture.

| Setting | Default | Description |
|---|---|---|
| Display Speed Controls | On | Shows the camera speed controls in the lower left of the preview. |
| Display Camera Controls | On | Shows the rotation arrows on the edges of the preview. |
| Show Crosshair | On | Shows a crosshair in the center of the preview. |
| Crosshair Color | Black | The color of the crosshair. |
| Crosshair Size | `15` | The size of the crosshair in pixels. |
| Show Frame | On | Shows frame corners in the preview. |
| Frame Color | White | The color of the frame corners. |
| Frame Size | `512` | The size of the frame in pixels. At least `50`. |
| Draw Grid | Off | Draws a grid in the preview scene. |
| Draw Axes | Off | Draws the world axes in the preview. |

## Workflow
| Setting | Default | Description |
|---|---|---|
| Show Notifications | On | Shows a notification with the name of each new thumbnail. Click the name to find it in the Content Browser. |
| Highlight Thumbnails | Off | Selects each new thumbnail in the Content Browser. |
| Suppress Overwrite Dialog | Off | Overwrites existing thumbnails without asking. |
