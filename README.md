# OCR Text Recognition

A web application that extracts text from images using an OCR (Optical Character Recognition) API. This application demonstrates API integration, file handling, and text processing.

## Features

- Upload an image to extract text
- Display recognized text in a readable format
- Error handling for API communication issues
- Simple and responsive user interface

## Technology Stack

- Frontend: HTML, CSS, Tailindcss, JavaScript
- Backend API Integration: Fetch API (JavaScript)
- OCR API Service: External OCR API

## API Integration

This application uses an external OCR API for text recognition. The API processes images and returns extracted text.

Key API features utilized:
- Image-to-text conversion
- Support for multiple image formats
- High accuracy in text detection

## Local Setup

1. Clone this repository:
```bash
git clone https://github.com/Strixx-thierry/Handwritten-Note-to-Pdf.git
cd Handwritten-Note-to-Pdf
```

2. Open `processImage` function in `script.js` and update the API endpoint and key:
```javascript
const response = await fetch("https://pen-to-print-handwriting-ocr.p.rapidapi.com/recognize/", {
    method: "POST",
    headers: {
        "x-rapidapi-key": "APIKEY",
        "x-rapidapi-host": "pen-to-print-handwriting-ocr.p.rapidapi.com"
    },
body: formData
});
```

3. Open `index.html` in a browser to test the application.

## Deployment

To deploy the application:

1. Upload the project files to a web server.
2. Ensure CORS policies allow API requests.
3. Use a hosting service like Netlify, Vercel, or an Nginx server for deployment.

## Challenges and Solutions

### Challenge 1: File Upload Handling
**Problem**: Ensuring the image file is properly sent to the API.
**Solution**: Used `FormData` in JavaScript to append and send the file securely.

### Challenge 2: API Response Format Variations
**Problem**: Different APIs return text in various structures.
**Solution**: Implemented conditional checks to handle multiple response formats.

### Challenge 3: CORS Restrictions
**Problem**: Some browsers block direct API requests due to CORS policies.
**Solution**: Used a proxy server to forward API requests securely.

## Future Improvements

- Support multiple OCR API providers
- Implement handwriting recognition
- Allow bulk image uploads for batch processing
- Add support for different languages

## Credits

- OCR API Service Provider
- Open-source libraries used in development