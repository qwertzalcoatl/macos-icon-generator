# macOS App Icon Generator

## About This Project

This Python script generates macOS app icons with the correct shape and sizes. I created it for a side project because I was tired of relying on half-paid Mac App Store icon generators.

## Credit and Inspiration

This implementation is based on the outstanding work done by Liam Rosenfeld, as detailed in his blog post ["My Quest for the Apple Icon Shape"](https://liamrosenfeld.com/posts/apple_icon_quest/). Liam's work in reverse-engineering the exact mathematics behind macOS app icons is truly impressive. He has build his own Icon generator, but I couldn't access it at the time of writing this. 

In any case, if you're interested in the deep dive into the geometry and math behind these icons, I highly recommend reading Liam's original post. 

## Why This Exists

- **Cross-platform:** Works on any system with Python, not just macOS.
- **No Dependencies on Mac-specific Tools:** Avoids the need for Xcode or other macOS-only software.

## Usage

## Usage

### Prerequisites

Ensure you have Python installed on your system along with the required libraries:

```bash
pip install pycairo Pillow
```

### Basic Usage

Run the script from the command line with your input image:

```bash
python macos_icon_generator.py path/to/your/input/image.png
```

This will generate icons in all standard macOS app icon sizes (16x16 to 1024x1024) and save them in the current directory.

### Specifying Output Directory

To save the generated icons in a specific directory:

```bash
python macos_icon_generator.py path/to/your/input/image.png -o path/to/output/directory
```

### Parameters

- `path/to/your/input/image.png`: Path to your high-resolution input image (required)
- `-o` or `--output`: Path to the directory where you want to save the generated icons (optional, defaults to current directory)

### Output

The script will generate the following icon sizes:
- 16x16
- 32x32
- 64x64
- 128x128
- 256x256
- 512x512
- 1024x1024

Each icon will be saved as a separate PNG file named `icon_SIZExSIZE.png` (e.g., `icon_512x512.png`).

### Example

```bash
python macos_icon_generator.py my_app_icon.png -o ./app_icons
```

This will take `my_app_icon.png`, generate all sizes of macOS app icons, and save them in the `./app_icons` directory.

## Disclaimer

This project is for personal and educational use. It's not affiliated with or endorsed by Apple Inc. The mathematical formulation of the icon shape is based on publicly available information and remains Apple's intellectual property.

## Appreciation

A big thank you to Liam Rosenfeld for sharing his work. This script is merely a practical Python implementation of his findings, nothing added by myself.
