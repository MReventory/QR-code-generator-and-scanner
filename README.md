# QR Code Generator & Scanner 🌈

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

A modern web application for generating and scanning QR codes. Features gradient UI design and smooth interactions.

## ✨ Features

- **Gradient UI Design** - Cyberpunk-inspired color scheme
- **QR Generation** - Convert text/URLs to QR codes instantly
- **File Scanning** - Upload and decode QR code images
- **Responsive Design** - Works on all device sizes
- **Modern Interactions** - Smooth animations and hover effects

## 🛠 Technologies Used

- **Frontend**: HTML5, CSS3 (Animations/Grid/Flex), JavaScript
- **Styling**: Glassmorphism, Neumorphism

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome 90+, Firefox 88+, Edge 90+)
- Local server (for full functionality)

### Installation

1. **Clone the repository**
```bash

git clone [https://github.com/YOUR-USERNAME/qr-code-generator-scanner.git](https://github.com/MReventory/QR-code-generator-and-scanner.git)
cd QR-code-generator-and-scanner
```

2. **Start a local server** (Choose one method):

   **Python Server**:
   ```bash
   python3 -m http.server 8000
   ```

   **VS Code Live Server**:
   - Install [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
   - Right-click `index.html` → "Open with Live Server"

   **Node.js http-server**:
   ```bash
   npx http-server
   ```

3. **Open in browser**:
   - Generator: `http://localhost:8000`
   - Scanner: `http://localhost:8000/scan.html`

## 🖥 Usage

### Generating QR Codes
1. Enter text or URL in the input field
2. Click "Generate QR Code"
3. Download/Share the generated QR code
4. Click the displayed link to verify

### Scanning QR Codes
1. Click "Choose File" to upload an image
2. Select a QR code image (PNG/JPG)
3. View decoded text below the form
4. Click detected links to open

⚠️ **Note**: Requires backend API endpoints at:
- `/generate_qr` (POST) - QR generation
- `/scan_qr` (POST) - QR decoding

## 🔧 API Requirements (For Full Functionality)

Implement these endpoints using your preferred backend technology (Node.js/Flask/Django):

```python
# Example Flask endpoint
@app.route('/generate_qr', methods=['POST'])
def generate_qr():
    data = request.form.get('data')
    # Generate QR code and return image URL
    return jsonify({'image_url': qr_path, 'text': data})
```

Recommended libraries:
- Python: `qrcode`, `opencv-python`
- Node.js: `qrcode`, `qr-image`

## 🚨 Troubleshooting

| Issue | Solution |
|-------|----------|
| CORS errors | Use local server instead of file:// protocol |
| Buttons not working | Check browser console (F12) for errors |
| QR not scanning | Ensure image contains valid QR code |
| Styling issues | Clear browser cache (Ctrl+Shift+R) |

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## ✉️ Contact

Ali Hemati - mreventory11@gmail.com

Project Link: [https://github.com/MReventory/QR-code-generator-and-scanner/](https://github.com/MReventory/QR-code-generator-and-scanner/)

## 🙏 Acknowledgements

- [Inter Font](https://rsms.me/inter/) - Beautiful typeface
- [Glassmorphism Effect](https://glassmorphism.com/) - UI inspiration
