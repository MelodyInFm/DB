# DB 

A Python GUI tool for creating glitch art (databending) on PNG images. Apply multiple effects in a stack, use masks, control effect intensity with mix, and save presets.

## Features

- Effect stack – add, remove, reorder effects. Each effect has its own parameters.
- Mix control – every effect has a mix parameter (0–1) to blend the effect with the original image.
- Masks – draw rectangles or polygons to limit effects to specific areas. Invert mask mode (inside/outside).
- Presets – save and load effect stacks as JSON files.
- Random chain – generate a random stack of 2–10 effects with random parameters.
- Real-time preview – original and result shown side by side.
- Dark theme – black/red interface with readable input fields.

## Available Effects

- Noise
- Bit Shift (bits, channel, direction)
- Channel Swap (channel order)
- Pixel Sort (rows or columns, fraction, reverse, metric)
- RGB Shift (horizontal/vertical shift)
- Block Shift (move random blocks)
- Bit Plane Slice (select bit plane)
- Invert (all or specific channel)
- Stripes (moving stripes)
- Posterize (reduce colour levels)
- Brightness / Contrast
- Saturation
- Pixelate
- Wave (sine distortion)
- Edge Detect
- Halftone (dot pattern)

## Requirements

- Python 3.8 or higher
- Pillow (PIL)
- NumPy

Install dependencies:

pip install pillow numpy


## Usage

1. Place the script in a folder with PNG files (or open any PNG via the "OPEN" button).
2. Run the script: `python DB.py`
3. Select an effect from the dropdown and click + ADD.
4. Adjust parameters using sliders, checkboxes, or dropdowns.
5. Use UP/DOWN to reorder effects or REMOVE to delete.
6. Apply a mask: select an effect, click MASK, draw a rectangle or polygon, then press F to finish.
7. Use IN/OUT to toggle whether the effect applies inside or outside the mask.
8. Save the result as PNG – click SAVE GLITCH and choose a folder.
9. Save / load your effect stack as a preset (JSON).

## Keys for Mask Drawing

- R – Rectangle mode (click-drag-release)
- P – Polygon mode (click to add points, double-click to close)
- F – Finish mask
- C – Clear all shapes

## File Structure

- The script auto-detects PNG files in its own directory.
- Saved images are named original_glitched.png (or with a counter if the file already exists).
- Presets are saved as .json files.

## Notes

- Effects are applied sequentially in the stack order.
- Masks are stored in memory per effect and are not exported to JSON presets.
- The mix parameter allows you to gradually increase the effect strength.

## License

MIT License.
