---
sidebar_position: 5
description: Capture thumbnails of many assets at once, and save the settings and camera as presets that can be shared with your team.
---

# Batch Capture and Presets

## Capturing several assets
Thumbnailer can capture a thumbnail of many assets in one go. Every asset is captured with the current settings, scene and camera rotation in the Thumbnailer window.

**Selected assets**
1. Select the static meshes, skeletal meshes and actor Blueprints in the Content Browser.
2. Right-click and select **Capture Thumbnails (N)**.

**Whole folders**
1. Right-click one or more folders in the Content Browser.
2. Select **Capture Thumbnails**. Every static mesh, skeletal mesh and actor Blueprint in the folders and their subfolders is captured.

The Thumbnailer window opens if it isn't open already, and a notification shows the progress. Click **Cancel** in the notification to stop after the current thumbnail. When the batch has finished, the notification shows how many thumbnails were captured and how many failed.

:::tip
Set up the first asset in the window before you start: pick a camera view, adjust the lighting and check the output settings. The batch uses the same settings for every asset.
:::

### Framing
By default each asset is framed from the current camera rotation, so every asset fills the thumbnail. Turn off **Frame Each Asset** under **Settings → Camera** to keep the camera where it is instead. Every asset is then captured from the same location, so they keep their size relative to each other.

### Existing thumbnails
If some of the thumbnails already exist, you are asked once for the whole batch:

| Answer | Result |
|---|---|
| **Yes** | Overwrites the existing thumbnails. |
| **No** | Skips the assets that already have a thumbnail. |
| **Cancel** | Doesn't start the batch. |

Turn on **Suppress Overwrite Dialog** to always overwrite without asking.

During a batch, **Override Thumbnail Name** is ignored, and no notification is shown for each thumbnail.

## Presets
A preset saves the settings, the camera and the scene profile as an asset in your project. Presets are saved in Content, so they can be shared with your team through source control, unlike the settings which are saved per user.

The **Preset** section is at the top of the right panel.

| Button | Description |
|---|---|
| Preset picker | Select a preset to apply it. Thumbnailer remembers the last selected preset. |
| **Apply** (refresh icon) | Applies the selected preset again, for example after you changed some settings. |
| **Save** (save icon) | Saves the current settings, camera and scene profile as a preset. Pick an existing preset to overwrite it. |

A preset contains:

| Category | Settings |
|---|---|
| Camera | Camera type, field of view, **Frame Each Asset**, camera rotation and location |
| Scene | The preview scene profile. Leave it empty to keep the current profile. |
| Output | Resolution, file format, save folder, file prefix, transparent background and editor billboards |
| Rendering | The anti-aliasing, auto exposure, motion blur, screen space reflections and eye adaptation settings |

Open the preset asset to change its values. When **Frame Each Asset** is on, the camera location is not used and the asset is framed from the camera rotation.

:::info
Presets are editor-only assets. They are never included in a packaged game.
:::
