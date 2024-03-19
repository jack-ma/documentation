---
sidebar_position: 7
---

import Display from "../../../common/radxa-os/\_display.mdx";

# Display Setting

Display setting is just available when you operating on the monitor, you can change the display setting by following ways.

## System Settings-Display Settings

On the XFCE desktop, left-click `Applications` in the upper left corner, you can see `Settings`, click `Display` to enter the display settings

![Display settings](/img/zero/zero3/radxa-display-xfce-1.webp)

![Display settings](/img/zero/zero3/radxa-display-xfce-2.webp)

## Terminal Command Settings

We also provide `xrandr` for display settings.
With the following command you can check the current display status:

```bash
xrandr
```

There is an example:

```bash
radxa@rock-5a:~$ xrandr
Screen 0: minimum 320 x 200, current 1920 x 1080, maximum 16384 x 16384
HDMI-1 connected primary 1920x1080+0+0 (normal left inverted right x axis y axis) 0mm x 0mm
   1920x1080     60.00*+  60.00    50.00    59.94
   1920x1080i    60.00    60.00    50.00    59.94
   1600x900      60.00
   1280x1024     75.02    60.02
   1152x864      75.00
   1280x720      60.00    60.00    50.00    59.94
   1024x768      75.03    60.00
   800x600       75.00    60.32
   720x576       50.00
   720x576i      50.00
   720x480       60.00    60.00    59.94    59.94    59.94
   720x480i      60.00    59.94
   640x480       75.00    60.00    59.94    59.94
   720x400       70.08
DP-1 disconnected (normal left inverted right x axis y axis)
```

You can check which monitor is connected and the corresponding resolution.

## Display Rotation

You can rotate your screen display by modifying the [Display Settings](display#system-settings-display-settings)-Orientation.
Or you can also achieving by command:

```bash
Single Screen:
   xrandr -o left     # Rotate 90 degrees to the left
   xrandr -o right    # Rotate 90 degrees to the right
   xrandr -o inverted # Flip up and down, rotate 180 degrees
   xrandr -o normal   # Back to the normal angle
   xrandr -s 1024x768 # Set the resolution
   xrandr -s 0        # Set the default resolution, which generally defaults to the highest resolution
   xrandr -rate       # Set refresh rate
```

## Multiple Screen Settings

In addition to Settings, the following commands enable you to modify in the display settings:

```bash
Dual Screen:
   # HDMI-1 --screen 1   DP-1 --screen 2
   xrandr --output HDMI-1 --primary # SetUp Home Screen
   xrandr --output HDMI-1 --auto --output DP-1 --off # Display only HDMI
   xrandr --output DSI-1 --off --output HDMI-1 --off # No display on either screen
   xrandr --output HDMI-1 --same-as DP-1 --auto # Simultaneous display of the same content
   xrandr --output HDMI-1 --right-of DP-1 --auto # DP-1 is the main display, the HDMI-1 is an extension and to the right of DP-1
```

For more information , please check [X.Org Server RandR](https://en.wikipedia.org/wiki/X.Org_Server#Other_DDX_components).
