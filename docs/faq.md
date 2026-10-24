---
sidebar_position: 3
sidebar_label: FAQ & Troubleshooting
description: Answers to common questions and problems with the Thumbnailer plugin.
---

# FAQ & Troubleshooting

## Capture Thumbnail says "No asset selected as screenshot source"
No asset is selected. Pick a static mesh, skeletal mesh or actor class on the **Asset** tab first.

## The background is not transparent
- Check that **Custom Depth-Stencil Pass** is set to **Enabled on Demand** or **Enabled with Stencil** in **Project Settings → Engine → Rendering**.
- Check that **Transparent** is checked under **Output**. The **Transparent** badge is shown in the preview when it is.
- The preview always shows the background. Only the captured thumbnail is transparent.

See [Transparent Thumbnails](/docfiles/guides/transparent-thumbnails).

## Parts of my actor are missing in a transparent thumbnail
Every component that should be visible needs **Render CustomDepth Pass** turned on in the actor Blueprint. See [Actors](/docfiles/guides/transparent-thumbnails#actors).

## My mesh disappears in a transparent thumbnail
The mesh has Nanite turned on, and a red warning is shown below the preview. Turn off **Nanite Support** on the mesh, or capture it without a transparent background. See [Nanite](/docfiles/guides/transparent-thumbnails#nanite).

## The HDR badge is shown in the preview
The editor renders in HDR, for example because HDR display output is turned on. The thumbnail is then saved as EXR, TGA is not available, and transparent backgrounds don't work. Turn off HDR display output to capture PNG, TGA or transparent thumbnails.

## The thumbnail looks blurry or different from the preview
- Keep **Disable Anti Aliasing**, **Disable Auto Exposure** and **Disable Motion Blur** on under **Settings → Rendering**.
- Turn on **Disable Eye Adaption** if the brightness changes between captures.
- The texture uses `2D Pixels (unfiltered)` and no mipmaps. If you show the thumbnail much smaller than its resolution, capture it at a lower resolution or change the texture settings.

## Where are my thumbnails?
In `/Game/Thumbnails` by default. The folder is set with **Save Dir**, and the lower right corner of the window shows where the next capture goes. Click the notification, or the browse button under **Last Capture**, to find the texture in the Content Browser. See [Output and Naming](/docfiles/guides/output).

## The capture timed out
A notification says `Thumbnail capture timed out` if the capture is not done after 10 seconds. This can happen the first time you capture a transparent thumbnail while shaders are still compiling. Wait for the shaders to finish and capture again.

## My settings are different in another project or on another computer
The settings are saved per user and per project in `EditorPerProjectUserSettings.ini`, and are not shared through source control. See [Settings](/docfiles/reference/settings).

## Can I capture several assets at once?
No, the plugin captures one asset at a time. Use [camera bookmarks](/docfiles/guides/camera#camera-bookmarks) to capture many assets from the same angle quickly.

## Is the plugin included in my packaged game?
No. Thumbnailer is an editor plugin. Only the textures it creates are packaged, like any other texture.
