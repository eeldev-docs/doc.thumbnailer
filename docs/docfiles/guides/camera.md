---
sidebar_position: 1
description: Frame the asset with camera views, focus, saved views and camera bookmarks, and switch between a perspective and an orthographic camera.
---

# Camera and Framing

## Moving the camera
The preview works like an editor viewport. Click the preview first so it has keyboard focus.

| Input | Action |
|---|---|
| Right mouse button + drag | Rotate the camera |
| Right mouse button + `W` `A` `S` `D` | Move and rotate the camera |
| Right mouse button + mouse wheel | Change the camera speed |
| `Alt` + left mouse button | Orbit around the asset |
| Arrows on the preview edges | Rotate the camera in 5° steps |
| **− / +** in the lower left | Change the camera speed |

All key bindings are listed in [Keyboard Shortcuts](/docfiles/reference/keyboard-shortcuts), and in the window under the **?** button.

## Focus and camera views
- **Focus** (`F`) frames the whole asset and keeps the current camera angle.
- The **Camera View** buttons on the right frame the asset from a fixed angle: **Front**, **Back**, **Top**, **Left**, **Right** or **Iso** (isometric, from above at 45°). The button of the current view is highlighted until you move the camera. The default view is **Iso**.

Both use the bounds of the asset, so the result is the same for small and large assets.

## Default view
- **Reset** (`R`) moves the camera to the default view.
- **Save View** in the bottom bar saves the current view as the new default view.

## Camera bookmarks
Save up to ten camera positions and jump between them. This is useful when you capture many assets of the same size from the same angle.

| Action | Keyboard | Bottom bar |
|---|---|---|
| Save the current view to a bookmark | `Ctrl` + `0`–`9` | Ctrl+click a number |
| Move the camera to a bookmark | `0`–`9` | Click a number |

The numbers of saved bookmarks are highlighted in the bottom bar. The bookmarks and the default view are saved per user and project, and are kept when you restart the editor.

## Perspective or orthographic
Set **Camera Type** under **Settings → Camera**.

| Camera Type | Description |
|---|---|
| **Perspective** | A normal camera. Use **Field of View (FOV)** to change the perspective. A smaller field of view gives a flatter, more 2D-like look. |
| **Orthographic** | No perspective at all, which suits icons and 2D games. **Field of View** is not used. |

The camera frames the asset again when you switch camera type.

## Framing aids
These are only shown in the preview and are never part of the capture. Change them under **Settings → Viewport**.

- **Crosshair** in the center of the preview, with a color and size.
- **Frame corners**, with a color and size, for example to mark a safe area.
- **Grid** and **axes** in the preview scene.
- The **camera speed** and the **rotation arrows** can be hidden.
