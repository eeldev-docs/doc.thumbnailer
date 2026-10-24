---
sidebar_position: 4
description: Set the resolution, file format, folder and name of the captured thumbnails, and how they are imported.
---

# Output and Naming

## Resolution
Set **Resolution** under **Output** in the right panel. The thumbnail can have any width and height, for example `512 x 512` or `1024 x 256`.

The preview is resized to the resolution, so you see the final aspect ratio while framing. Each side of the preview is limited to between 150 and 1024 pixels. The capture always uses the full resolution.

## Format
| Format | Description |
|---|---|
| **PNG** | The default. |
| **TGA** | The capture is converted to TGA before it is imported. |

When the editor renders in HDR, the capture is saved as EXR. TGA is not available for HDR captures.

## Folder
Thumbnails are imported to `/Game/Thumbnails` by default. Change **Save Dir** under **Settings → Output** to use another folder in your project's Content folder, for example `UI/Icons` for `/Game/UI/Icons`. The folder is created if it doesn't exist.

The lower right corner of the window shows the file name of the next capture and the folder it is imported to.

## Name
The name of the texture is the **File Prefix** followed by the name of the asset:

| Asset | File Prefix | Texture |
|---|---|---|
| Static mesh `SM_Chair` | `Thumb_` | `Thumb_SM_Chair` |
| Actor Blueprint `BP_Door` | `Icon_` | `Icon_BP_Door` |

To use another name for the next captures, enter it in **Override Thumbnail Name** under **Settings → Output**. It replaces the asset name and is cleared when the editor restarts.

Characters that can't be used in an asset name are replaced.

## Overwriting thumbnails
If a texture with the same name exists, you are asked whether to overwrite it. Turn on **Suppress Overwrite Dialog** under **Settings → Workflow** to always overwrite without asking.

## How the thumbnail is imported
1. The preview is captured as a high resolution screenshot to a folder under `Saved/Screenshots` in your project.
2. The screenshot is converted to TGA if you selected TGA.
3. The file is imported as a texture to the **Save Dir** folder.

The texture is set up for UI:

| Texture setting | Value |
|---|---|
| Texture Group | `2D Pixels (unfiltered)` |
| Mip Gen Settings | `NoMipmaps` |

Remember to save the new texture. It is marked as modified after the import.

## Notifications
| Setting | Default | Description |
|---|---|---|
| Show Notifications | On | Shows a notification with the name of each new thumbnail. Click the name to find it in the Content Browser. |
| Highlight Thumbnails | Off | Selects each new thumbnail in the Content Browser. |
