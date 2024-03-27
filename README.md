# Image to ASCII Art Converter

This program converts an image into ASCII art. It takes an input image file and generates a corresponding ASCII representation, which can be saved to an output text file.

## Usage

```
python ascii_converter.py --file <input_image_file> [--scale <scale_factor>] [--out <output_file>] [--cols <num_columns>] [--morelevels]
```

### Arguments

- `--file`: **(Required)** Specifies the input image file.
- `--scale`: *(Optional)* Specifies the scale factor for the output ASCII art. Default value is 0.43, which suits a Courier font.
- `--out`: *(Optional)* Specifies the output file name. Default is `out.txt`.
- `--cols`: *(Optional)* Specifies the number of columns for the ASCII art. Default is 80.
- `--morelevels`: *(Optional)* Adds more levels of gray for better representation. If provided, it uses 70 levels of gray; otherwise, it uses 10 levels of gray.

## Requirements

- Python 3.x
- PIL (Python Imaging Library)

## How It Works

1. Open the input image file and convert it to grayscale.
2. Determine the dimensions of the image and calculate the dimensions of each tile based on the specified number of columns and scale factor.
3. Iterate through each tile of the image, calculate the average luminance, and map it to an ASCII character based on the grayscale level.
4. Generate the ASCII representation of the image as a list of character strings.
5. Write the ASCII art to the output file.

## Example

To convert an image named `input.jpg` to ASCII art with 100 columns and a scale factor of 0.5, you can run:

```
python ascii_converter.py --file input.jpg --cols 100 --scale 0.5
```

## Credits

- The grayscale level values used for mapping luminance to ASCII characters are sourced from [Paul Bourke's website](http://paulbourke.net/dataformats/asciiart/).
- This code was written for educational purposes and inspired by various ASCII art tutorials and resources available online.
```
