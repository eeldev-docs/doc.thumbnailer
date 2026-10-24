---
sidebar_position: 2
description: Capture thumbnails with a transparent background, for meshes and for actor Blueprints.
---

# Transparent Thumbnails

A transparent thumbnail only contains the asset. The background, the floor and the sky are removed, so the thumbnail can be placed on any UI.

## Enable Custom Depth-Stencil Pass
Transparent thumbnails use the custom depth pass to find the asset. Open **Edit → Project Settings → Engine → Rendering** and set **Custom Depth-Stencil Pass** to **Enabled on Demand**, or **Enabled with Stencil**.

![Custom Depth-Stencil Pass in Project Settings](/img/transparent-1.png)

## Turn on Transparent
- Check **Transparent** under **Output** in the right panel. It is the same setting as **Transparent Thumbnail** under **Settings → Output**.
- The **Transparent** badge is shown in the upper left corner of the preview.

The preview still shows the background. It is removed when you capture.

## The result
The thumbnail is imported as a texture with an alpha channel.

![A transparent thumbnail](/img/transparent-3.png)

## Actors
Static and skeletal meshes are set up by the plugin. An actor Blueprint needs one change: every component that should be visible in the thumbnail must have **Render CustomDepth Pass** turned on. Components without it are removed together with the background.

- Open the actor Blueprint, select each mesh component and turn on **Rendering → Render CustomDepth Pass**.

![Render CustomDepth Pass on the actor components](/img/transparent-actor-1.png)

![A transparent actor thumbnail](/img/transparent-actor-2.png)

## Nanite
Transparent thumbnails don't work with Nanite meshes. A red warning is shown below the preview when the selected static mesh has Nanite turned on.

- Open the static mesh and turn off **Nanite Support**, or capture it without a transparent background.

## HDR
Transparent backgrounds don't work when the editor renders in HDR, for example when HDR display output is turned on. The **HDR** badge is shown in the upper right corner of the preview when this is the case. Turn off HDR display output to capture transparent thumbnails.
