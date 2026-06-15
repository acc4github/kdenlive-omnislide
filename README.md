# OmniSlide - Frei0r Transition Plugin for Kdenlive

A frei0r-based, extremely versatile slide transition plugin for Kdenlive. It's designed to cover pretty much any slide/swipe-related transitions.

## Features

- **Arrival Direction Axis / Wheel**: Controls the angles at which the incoming clip enters.
- **Departure Direction Axis / Wheel**: Controls the angles at which the outgoing clip disappears (when moving).
- **Outgoing Behavior**: Static / Move / Fade.
- **Speed Curve (%)**: Higher % = stronger acceleration.
- **Gentle Arrival (%)**: Add smooth slowdown to the clip's movement. It switches between 2 mechanisms depending on the Speed Curve's state.
  - **When Speed Curve is at 0%**: Gentle Arrival acts like a reverse Speed Curve, adding a negative logarithmic curve to the speed. As you dial up Gentle Arrival, the curve will become stronger, and clips will start fast and decelerate towards the end. 
  - **When Speed Curve is used**: Gentle Arrival's intensity will symmetrically mirror Speed Curve's logarithmic curve. And as you dial up Gentle Arrival, it will expand the 'effective zone' from the clip's end. The clips will start to slow down as the playback enters this zone. At 100%, the entire clip is under Gentle Arrival's control.
- **Motion Blur (%)**: Add directional blur to the moving clips. (The current motion blur is very low-res to prioritize performance. I didn't add controls for blur quality since I thought it was not that important, but I might later...)
- **Edge Smoothing**:
  - **ON**: Smoothing out the clip's edge pixels. (Note that it introduces dark edges on blurred clips due to Kdenlive's limitation.) 
  - **OFF**: The clip's boundaries are exactly snapped to its actual content.
- **Invert**: Invert the effect.

## Installation (Windows)

1. Download the build from the release. The zip file should have `omni-slide.dll` and `omni-slide.xml`.
2. Place `omni-slide.dll` in Kdenlive frei0r plugins folder (e.g., kdenlive-master\lib\frei0r-1)
3. Place `omni-slide.xml` in Kdenlive effects folder (e.g., kdenlive-master\bin\data\kdenlive\transitions)
4. Restart Kdenlive. The transition should appear under "Transitions".

## License

This project is licensed under the **GNU General Public License v3.0** (GPL-3.0).
See the LICENSE for full details.

## Credits

Developed for the open-source video editing community.  
Copyright (C) 2026 acc4commissions