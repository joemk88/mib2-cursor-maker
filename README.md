## MIB2 2D Cursor Maker

This is a simple GUI tool for creating custom navigation cursors for Audi/VW MIB2 systems using a transparent PNG (builds objects.cff automatically).

This project automates the full workflow required to build a valid `objects.cff` file — no manual hex editing or reverse engineering required.

Originally developed through reverse engineering of the MIB2 cursor format, this tool converts a user-provided image into a working in-car navigation cursor.


## How It Works

MIB2 navigation cursors are stored inside an `objects.cff` container.

This tool:
1. Takes a transparent **256×256 PNG**
2. Inserts it into the cursor shadow texture
3. Builds a new `carsorshadow.sfc`
4. Repackages everything into a valid `objects.cff`

The original 3D cursor is made invisible, allowing the PNG to act as a clean 2D navigation marker.


## Usage

1. Launch `carsor_gui.py`
2. Select a 256×256 transparent PNG
3. Click **Build**
4. Rename the output file to `objects.cff`
5. Copy to your MIB2 system


## Requirements

- Python 3.10+


## Compatibility

Tested on:

- Audi MIB2 High
- Audi A3 (MY19)

Should work on most MIB2 units including:
Audi / Volkswagen / Skoda / Seat systems using `objects.cff`.


## Disclaimer

This project is provided for educational and customization purposes only.

You are responsible for any modifications made to your vehicle.
Always keep backups of original files before installing custom content.

This project is not affiliated with Audi AG, Volkswagen Group, or any related manufacturers.


## Credits

Reverse engineering and tooling by the community.
Special thanks to: @jilleb @superkolos @hgnme
Special thanks to MIB2 modding forums and contributors who documented container formats and firmware behaviour.


