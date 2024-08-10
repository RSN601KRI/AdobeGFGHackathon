# Curvetopia: A Journey into the World of Curves

Welcome to **Curvetopia**, a project designed to bring order and beauty to the world of 2D curves. This project focuses on identifying, regularizing, and beautifying curves in 2D Euclidean space, starting with simple closed curves and extending to more complex shapes.

## Objective

Our mission is to process polylines (sequences of points) from input CSV files and convert them into smooth curves represented by cubic Bezier curves. The project also involves tasks like symmetry analysis and curve completion for occluded shapes.

## Problem Description

We start with polylines and aim to convert them into cubic Bezier curves. The main steps are:

1. **Input Handling**: Read polylines from CSV files.
2. **Curve Regularization**: Convert polylines to cubic Bezier curves or use linear interpolation if the polyline has fewer than 8 points.
3. **Symmetry Analysis**: Analyze the shapes for regularity and symmetry.
4. **Curve Completion**: Handle occlusions by completing curves based on neighboring shapes.
5. **Output Generation**: Generate SVG files for visualization and rasterize them to PNG format for validation.

## File Structure

- `read_polylines`: Reads polylines from a CSV file.
- `polyline_to_bezier`: Converts polylines to Bezier curves, handling cases with fewer than 8 points using linear interpolation.
- `generate_svg`: Creates an SVG file from the Bezier curves.
- `rasterize_svg`: Converts the SVG file to a PNG image.
- `process_polylines`: Main function to process input CSV files and generate output files.

## Requirements

Ensure you have the following Python packages installed:
- `numpy`
- `pandas`
- `svgwrite`
- `scipy`
- `matplotlib`
- `PIL` (Pillow)

You can install these packages using pip:

```sh
pip install numpy pandas svgwrite scipy matplotlib pillow
```

## Usage

1. **Prepare Your Data**: Ensure your input CSV files contain the polylines data in the required format.

2. **Run the Code**: Use the provided Python script to process your data. Modify the `input_csv` and `output_svg` variables to point to your specific files.

```python
input_csv = 'path/to/your/input.csv'
output_svg = 'path/to/your/output.svg'
process_polylines(input_csv, output_svg)
```

3. **Check Results**: The script will generate an SVG file and a PNG file. The SVG file contains the visual representation of the curves, while the PNG file can be used for validation.

## Example

For example, if you have an input file `frag0.csv`, you can run:

```python
input_csv = 'frag0.csv'
output_svg = 'frag0.svg'
process_polylines(input_csv, output_svg)
```

This will create `frag0.svg` and `frag0.png` in the current directory.

## Notes

- The code currently handles polylines with fewer than 8 points using linear interpolation. For more advanced cases, additional methods may be required.
- Ensure that your CSV files are correctly formatted with sequences of points.

## Contributing

Contributions to the project are welcome! Please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details
