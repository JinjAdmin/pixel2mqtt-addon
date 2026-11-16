# pixel2mqtt

Bridge and web editor for **Govee H6631 Gaming Pixel Light** displays running the custom
[pixeld-h6631](https://github.com/SamWiIIiams/pixeld-h6631) firmware. One MQTT connection for any number of
displays, Home Assistant discovery, and an editor for animations and icons with live preview on the panel.

## Before you start
- Install the firmware on the display first (see the pixeld-h6631 README).
- Install the **Mosquitto broker** app (add-on), start it, and add the **MQTT** integration Home Assistant then
  offers. pixel2mqtt gets the broker login from it automatically, so there's nothing to type.

## Using it
1. Start the app. Open its web UI with **Open web UI**, or switch on **Show in sidebar** on the app's page to get
   a **Pixel displays** entry in the sidebar.
2. Under **Displays**, adopt your display: a pairing code appears on the panel.
3. Under **Library**, click **Import built-in animations & icons** to convert the artwork already on your display,
   including scenes you applied from the Govee app before installing the firmware.

The display then appears in Home Assistant as a device, with its controls and animations.

## Options
| Option | Default | |
|---|---|---|
| `base_topic` | `pixel2mqtt` | MQTT topic prefix for displays adopted from now on |
| `discovery_prefix` | `homeassistant` | Home Assistant's MQTT discovery prefix |
| `hosts` | `[]` | Display IP addresses to add if network discovery can't find them |
| `scan_interval` | `120` | Seconds between network scans for new displays |
| `allow_direct_access` | `false` | Also allow the web UI on port 8466 from your network (it has no login) |
| `mqtt_host` / `mqtt_port` / `mqtt_user` / `mqtt_password` | | Use a different broker instead of the Mosquitto add-on |

## Notes
- The add-on uses the host network so it can find displays and send live frames to them.
- No artwork is included. Imports read the files from your own display and write the results back to it.
- Unofficial; not affiliated with Govee.
