---
sidebar_position: 1
slug: /
description: Thumbnailer is an Unreal Engine editor plugin that captures thumbnails and icons of static meshes, skeletal meshes and actors, and imports them as textures.
---

# Introduction

## The Thumbnailer Plugin
Thumbnailer creates thumbnails and icons for your games and projects inside the Unreal Engine editor. Pick a static mesh, skeletal mesh or actor, frame it in the preview, and click **Capture Thumbnail**. The capture is imported straight into your project as a texture, ready to use in your UI.

![The Thumbnailer window](/img/thumbnailer-window.webp)

## Features
- **Capture static meshes, skeletal meshes and actor Blueprints.** Open them from the Content Browser with **Create Thumbnail**. See [Capturing a Thumbnail](/docfiles/getting_started/using-plugin).
- **Transparent backgrounds**, so the thumbnail can be placed on any UI. See [Transparent Thumbnails](/docfiles/guides/transparent-thumbnails).
- **Any resolution**, saved as PNG or TGA and imported as a texture with UI-friendly settings. See [Output and Naming](/docfiles/guides/output).
- **Camera views and bookmarks.** Frame the asset from the front, back, sides, top or an isometric angle with one click, and save up to ten camera positions on the number keys. See [Camera and Framing](/docfiles/guides/camera).
- **Batch capture.** Capture every selected asset, or every asset in a folder, in one go. See [Batch Capture and Presets](/docfiles/guides/batch-and-presets).
- **Presets** that save the settings, camera and scene profile as an asset you can share with your team.
- **Perspective or orthographic camera**, with an adjustable field of view.
- **A customizable preview scene**: lighting, environment, floor and post processing. See [Preview Scene](/docfiles/guides/preview-scene).
- **Framing aids** in the preview: a crosshair, frame corners, grid and axes.
- **Clean captures.** Anti-aliasing, auto exposure, motion blur and screen space reflections can be turned off while capturing, and editor billboards are hidden.
- **Last Capture** preview in the window, with a larger preview and buttons to open, find and copy the texture.

## Requirements
| | |
|---|---|
| Unreal Engine | 5.4 to 5.8 |
| Editor platforms | Windows, Mac, Linux |
| Runtime | Editor only. Nothing from the plugin is included in a packaged game, only the textures it created. |

:::note Older engine versions
Updates and new features are only released for Unreal Engine 5.4 and newer. Unreal Engine 4.27 to 5.3 use an earlier version of the plugin, which can still be downloaded from Fab but is no longer updated. The earlier version has a different Thumbnailer window, so parts of this documentation don't apply to it.
:::

## Where to go next
1. [Install the plugin](/docfiles/getting_started/installing-plugin)
2. [Capture your first thumbnail](/docfiles/getting_started/using-plugin)
3. Get to know [the Thumbnailer window](/docfiles/getting_started/thumbnailer-window)
4. Set up [transparent thumbnails](/docfiles/guides/transparent-thumbnails)
