# Gallery Customization Guide

This guide explains how to add your own photo and QR code to the badge gallery.

## Placeholder Images Included

Two placeholder images have been created for you to replace with your own:

1. **my-photo.png** - A placeholder for your personal photo
2. **my-qr-code.png** - A placeholder for your QR code

Each placeholder exists in two sizes:
- Full-size images (160x120 pixels) in `images/`
- Thumbnails (30x23 pixels) in `thumbnails/`

## How to Customize

### Step 1: Prepare Your Images

Create your own images with the following specifications:

#### Full-Size Images (160x120 pixels)
- **Your Photo**: Create or resize your photo to 160x120 pixels
- **Your QR Code**: Generate a QR code and resize it to 160x120 pixels
- Format: PNG with RGB color
- Recommended: Use image editing software or online tools to resize

#### Thumbnail Images (30x23 pixels)
- Create smaller versions of your images at 30x23 pixels
- These are displayed in the thumbnail strip at the bottom of the gallery
- Same filenames as full-size images

### Step 2: Replace the Placeholder Images

Replace the placeholder files with your own images, keeping the same filenames:

**Full-size images** (in `images/` directory):
- `my-photo.png` → Replace with your photo (160x120 pixels)
- `my-qr-code.png` → Replace with your QR code (160x120 pixels)

**Thumbnails** (in `thumbnails/` directory):
- `my-photo.png` → Replace with your photo thumbnail (30x23 pixels)
- `my-qr-code.png` → Replace with your QR code thumbnail (30x23 pixels)

## Deploying to Your Badge

Follow these steps to copy your customized gallery to your badge:

### 1. Enter USB Mass Storage Mode
- Double-press the **Reset** button on the back of your badge
- Your badge will appear as a USB drive named `BADGER`

### 2. Copy the Gallery App
Copy the entire gallery app directory structure to your badge:

```
BADGER/
└── apps/
    └── gallery/
        ├── images/
        │   ├── my-photo.png
        │   └── my-qr-code.png
        └── thumbnails/
            ├── my-photo.png
            └── my-qr-code.png
```

**Important**: You only need to copy the files you want to customize. The badge will use your versions instead of the pre-installed ones.

### 3. Eject and Reset
- Safely eject the `BADGER` drive
- Press **Reset** once to return to normal mode
- Your badge will boot with your custom images in the gallery!

## Using the Gallery App

1. From the main menu, navigate to and select the **Gallery** app
2. Use **A** button to scroll left through images
3. Use **C** button to scroll right through images
4. Press **B** button to toggle UI visibility (hide/show thumbnails and title)
5. Your photo and QR code will appear in the gallery rotation

## Tips

- **Image Quality**: For best results, ensure your images are exactly 160x120 pixels (full-size) and 30x23 pixels (thumbnails)
- **QR Codes**: Make sure your QR code has good contrast (black on white) and includes adequate error correction for the small display size
- **Photos**: Portrait photos work well. Consider adding a simple border or background color to fill the 160x120 frame
- **File Format**: Use PNG format with RGB color mode (no transparency needed)
- **Testing**: After copying files to your badge, test the gallery app to ensure images display correctly

## Adding More Images

You can add as many images as you want! Just follow the same pattern:
1. Create a full-size image (160x120 pixels) and save it in `images/`
2. Create a thumbnail (30x23 pixels) with the same filename in `thumbnails/`
3. The gallery app will automatically discover and display all PNG images in these directories

## Troubleshooting

- **Images don't appear**: Ensure filenames match exactly between `images/` and `thumbnails/` directories
- **Images look stretched**: Verify your images are exactly 160x120 (full) and 30x23 (thumb) pixels
- **Gallery is empty**: Make sure you copied the files to `/apps/gallery/` on the BADGER drive, not the root directory

## Example: Creating a QR Code

You can use online QR code generators to create your QR code:
1. Visit a QR code generator website (e.g., qr-code-generator.com)
2. Enter your desired content (URL, contact info, etc.)
3. Download the QR code as PNG
4. Resize to 160x120 pixels for full-size and 30x23 for thumbnail
5. Replace `my-qr-code.png` with your custom QR code

Enjoy your personalized badge! 🎉
