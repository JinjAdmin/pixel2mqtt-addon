# Changelog

## 0.5.0
Needs pixeld-h6631 v0.3.0 for info screens.
- **Info screens:** design layouts in the new screen editor (text, values, icons, bars, sparklines, shapes) and bind
  them to Home Assistant entities: state, attribute, history, fixed values and weather forecasts.
- **Template screens:** one layout for a group of similar entities (e.g. every stock ticker), picked in Home
  Assistant or rotating.
- **Exposed settings:** turn any screen setting (font, colour, a chart's time window, …) into a Home Assistant
  entity.
- Sparklines skip flat stretches and use long-term statistics for long windows; slow fetches no longer block MQTT.
- Editor: Sources tab, Expose toggles, one grid layout, LED-dot canvases, a font picker drawn at the panel's scale,
  icon size set in the icon editor.
- Library refresh; guide rewritten with a Screens chapter and screenshots.
- "Info" is now "Screens" / "screen rotation", matching pixeld v0.3.0.

## 0.4.3
- The editor canvas is now a workspace around the panel: zoom (mouse wheel or the - / + buttons), pan (middle-drag,
  Alt + drag or the pan button) and "Recenter on viewport".
- Draw layers bigger than the panel: the parts outside it are shown (other layers dimmed), so long scrolling
  backgrounds no longer repeat every 52 pixels. "Hide outside viewport" shows the panel only.

## 0.4.2
- Frames: shift a frame's pixels (Shift + arrow keys), or make a run of frames that each move a step, with
  "fit loop" for a seamless wrap.
- Loop hint next to the timeline: shows whether the scene loops seamlessly and which layer doesn't.
- New colour picker (no browser pop-up) and a palette of your last 18 colours.
- Styled dialogs instead of the browser's pop-ups.
- The built-in guide is rebuilt around a full example project, covering every editor feature.

## 0.4.1
- Editor guide built in: the **?** button at the top right opens it in a side drawer (works offline, matches
  the installed version).
- Frames: set one duration for every frame of a layer at once (Set all frames).

## 0.4.0
- Editor projects: a start screen, Save (and autosave) separate from Send to display, status Draft / On display /
  Changed since sent, warnings before replacing something on the display, export/import of project files.
- Tool settings in a flyout next to each tool; every tool keeps its own size, tip and colour.
- New Shape tool (rectangle, oval, triangle, diamond, trapezoid; outline or filled), brush sizes and round tips,
  tool-shaped cursors, a Clear button for layers, Scale for layers.

## 0.3.0
- First stable Home Assistant app (add-on): Ingress web UI, MQTT login from the Mosquitto app, data in the app's
  storage. Tested on Home Assistant OS 2026.11 (Raspberry Pi 5).

## 0.3.0-beta.1
- First Home Assistant add-on build: Ingress web UI, MQTT login from the Mosquitto add-on, data in the add-on's
  storage.
