# Number-Plate-Detection-with-OpenCV-and-Flask

### README File

## Project Description

This project demonstrates a web application for detecting number plates in images using OpenCV and PyTesseract for image processing and text extraction, and Flask for creating the web interface. Users can upload images through the web interface, and the application will process the image to detect the number plate and display both the original and processed images side by side.

## Features

- Upload images via a web interface
- Detect number plates using OpenCV
- Extract text from number plates using PyTesseract
- Display the original and processed images side by side
- User-friendly and visually appealing interface

## Prerequisites

- Python 3.x
- Flask
- OpenCV
- PyTesseract
- imutils
- A Tesseract installation (make sure to set the correct path)

## Setup Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/number-plate-detection.git
   cd number-plate-detection
   ```

2. **Install the required packages**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set up Tesseract**

   Make sure Tesseract is installed on your system. You can download it from [here](https://github.com/tesseract-ocr/tesseract).

   Update the path to Tesseract in the code:
   
   ```python
   pytesseract.pytesseract.tesseract_cmd = r"path_to_your_tesseract_executable"
   ```

4. **Run the Flask application**

   ```bash
   python app.py
   ```

5. **Open your web browser and navigate to**

   ```
   http://127.0.0.1:5000/
   ```

## Project Structure

- `app.py`: The main Flask application that handles image uploads, processing, and displaying results.
- `templates/upload.html`: The HTML template for the web interface.
- `uploads/`: Directory to store uploaded images.
- `processed/`: Directory to store processed images.
- `requirements.txt`: List of required Python packages.

## Code Explanation

1. **Image Upload and Processing**

   The Flask application allows users to upload an image through the web interface. The uploaded image is saved to the `uploads` directory.

2. **Image Processing with OpenCV**

   - The uploaded image is read and resized.
   - The image is converted to grayscale and smoothed using a bilateral filter.
   - Edge detection is performed using the Canny edge detector.
   - Contours are detected and sorted to find potential number plates.
   - The contour with four points (indicating a rectangle) is identified as the number plate.
   - The detected number plate is extracted and highlighted on the original image.

3. **Text Extraction with PyTesseract**

   - The extracted number plate image is processed with PyTesseract to extract the text.

4. **Display Results**

   The original and processed images are displayed side by side on the web interface.

## Contributing

Feel free to fork this repository, make improvements, and submit pull requests. Any contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Choose a title that best fits your vision for the project.
