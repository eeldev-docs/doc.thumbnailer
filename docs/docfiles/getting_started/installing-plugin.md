---
sidebar_position: 1
description: How to install the Thumbnailer plugin, enable it and move it to your project.
---

# Installing the plugin

The plugin is installed from the Epic Games Launcher.

## Locate the plugin
- Add the plugin to your library on [Fab](https://www.fab.com/listings/bc8998b0-f5da-4195-9ef1-4d6fb3fa802b).
- In the Epic Games Launcher, open **Unreal Engine → Library → Fab Library** and search for **Thumbnailer**.

![Locate the plugin](/img/installing-1.png)

## Select Engine Version
- Click **Install to Engine** and select the engine version to install it to.

![Select engine version](/img/installing-2.png)

:::note
Unreal Engine 4.27 to 5.3 get an earlier version of the plugin that is no longer updated. Use Unreal Engine 5.4 or newer to get the latest version. See [Requirements](/#requirements).
:::

## Verify plugin installation
- Verify that the plugin was installed.

![Plugin installed](/img/installing-3.png)
![Plugin installed in the engine](/img/installing-4.png)

## Enable the plugin
- Open **Edit → Plugins**, search for **Thumbnailer** and make sure it is enabled. Restart the editor if you are asked to.

![Plugin enabled](/img/using-1.png)

## Move the Plugin (Optional)
This step is optional, but we recommend moving installed plugins to your project's `Plugins` folder.

- Locate the plugin. A common install location is:

```
C:\Program Files\Epic Games\UE_5.x\Engine\Plugins\Marketplace
```

- Move the `Thumbnailer` folder to your project's `Plugins` folder. Create the `Plugins` folder if it doesn't exist.

:::info
Thumbnailer is an editor plugin. It is never included in a packaged game, so it is safe to keep it enabled in any project.
:::

## Next step
[Capture your first thumbnail](/docfiles/getting_started/using-plugin).
