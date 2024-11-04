# Image OCR and Medical Keyword Detection App
This repository hosts a Python Flask web application designed to process images, extract text using Optical Character Recognition (OCR), and detect the presence of medical-related keywords. The project can be useful for healthcare applications that require automated extraction and categorization of medical information from image data.

## Features
* **Image Upload and Processing:** Users can upload an image, which is then processed and analyzed for text extraction.
* **OCR Functionality:** Uses Tesseract OCR to extract text from images.
* **Medical Keyword Detection:** The extracted text is searched for predefined medical-related keywords to identify relevant terms.
* **RESTful API:** Provides an API endpoint for image upload and response in JSON format indicating if medical keywords were detected.

## Installation
Follow these steps to set up and run the application locally:

**1. Clone the Repository:**
```Bash
git clone https://github.com/yourusername/medical-ocr-keyword-app.git
cd medical-ocr-keyword-app
```
**2. Create a Virtual Environment (Optional but Recommended):**
```bash
python -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
```

**3. Install Dependencies:**
```bash
pip install -r requirements.txt
```

**4. Install Tesseract OCR: Ensure that Tesseract OCR is installed and configured:**
```bash
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```

**5. Run the Application:**
```bash
python app.py
```

## Usage
* Open your web browser and navigate to http://localhost:5000/.
* Use the /upload endpoint to upload an image for processing.
* The app will return a JSON response indicating if any medical keywords were found.

## API Endpoints
* GET /: Serves the index.html file (home page).
* POST /upload: Accepts an image file and returns a JSON response:
* True if medical keywords are found in the text.
* False if no keywords are found.

## Project Structure
```bash
your_project/
├── app.py                  # Main application script
├── requirements.txt        # List of dependencies
├── index.html              # Front-end file for the home route
└── README.md               # Project documentation
```

## Dependencies
* **Flask:** For building the web server.
* **Pillow (PIL):** For image processing.
* **pytesseract:** Python wrapper for Tesseract OCR.
* **re:** For keyword searching using regular expressions.
### Install all Python dependencies using:
```bash
pip install Flask Pillow pytesseract
```
