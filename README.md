# Fruit Ripeness Detection

This project uses image processing techniques to detect the ripeness of fruits by analyzing their color composition. The script reads an image of a fruit, processes it to detect edges, and then uses color thresholds to determine the amount of red, green, and yellow areas in the image. Based on these color areas, the ripeness of the fruit is evaluated.

## Prerequisites

- Python 3.6+
- OpenCV
- NumPy
- PIL (Python Imaging Library)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/fruit-ripeness-detection.git
    cd fruit-ripeness-detection
    ```

2. Install the required packages:

    ```sh
    pip install -r requirements.txt
    ```

    Ensure the `requirements.txt` includes:
    ```
    numpy
    opencv-python
    pillow
    ```

## Usage

1. Place the image of the fruit you want to analyze in the project directory. Update the script to use the correct image file.

    ```python
    image = np.array(Image.open('your_fruit_image.jpg'))
    ```

2. Run the script:

    ```sh
    python detect_ripeness.py
    ```

3. The script will display the processed image with edge detection and the masks for red, green, and yellow colors. It will also print the ripeness status based on the color analysis.

## Project Structure

- `detect_ripeness.py`: The main script for detecting fruit ripeness.
- `requirements.txt`: List of dependencies required to run the script.
- `images/`: Directory to store sample fruit images (not included).

## Methodology

1. **Edge Detection**: Detect edges in the image to find the contour of the fruit.
2. **Color Thresholding**: Apply color thresholds to create masks for red, green, and yellow areas.
3. **Area Calculation**: Calculate the area of each color mask.
4. **Ripeness Evaluation**: Determine the ripeness of the fruit based on the percentage of each color area.

## Sample Output

- Displays the edge-detected image and color masks.
- Prints the ripeness status:
    - "Need time to grow" if the green area is predominant.
    - "Medium Ripeness" if the yellow area is predominant.
    - "No Ripeness" if the red area is predominant.
    - "Not defined" for other cases.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

.
