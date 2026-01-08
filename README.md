
#  Hair Style Recommendation System



An AI-powered web application that analyzes facial features and provides personalized hairstyle recommendations using computer vision and deep learning.

##  Features

- **Real-time Face Analysis**: Automatic detection and classification of face shape, hair type, age category, and gender
- **Personalized Recommendations**: AI-driven hairstyle suggestions with maintenance levels
- **High Accuracy**: 90%+ detection success rate on clear frontal images
- **Fast Processing**: 1.8-4.2 seconds average response time
- **User-Friendly Interface**: Simple web-based upload and instant results
- **Privacy-Focused**: No user data storage, images deleted after processing

##  Demo

Upload a frontal facial photo → Get instant analysis → Receive personalized hairstyle recommendations!

##  Quick Start

### Prerequisites

- Python 3.10 or higher
- NVIDIA GPU (recommended for faster inference, but CPU works)
- 16 GB RAM (recommended)
- Windows, Linux, or macOS

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/hairstyle-recommendation.git
cd hairstyle-recommendation
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Download trained models**
   - Place your custom YOLOv8 model (`best.pt`) in the `models/` directory
   - Or download from: [Google Drive Link] (replace with actual link)

### Running the Application

1. **Start the Flask server**
```bash
python app.py
```

2. **Open your browser**
   - Navigate to `http://localhost:5000`
   - Upload a clear frontal facial photo
   - View your personalized recommendations!

##  Project Structure

```
hairstyle-recommendation/
│
├── app.py                      # Main Flask application
├── models/
│   └── best.pt                 # Trained YOLOv8 model weights
├── static/
│   ├── css/                    # Stylesheets
│   ├── js/                     # JavaScript files
│   └── uploads/                # Temporary image storage
├── templates/
│   └── index.html              # Main web interface
├── notebooks/
│   └── Hair_Style.ipynb        # Model training notebook
├── requirements.txt            # Python dependencies
├── README.md                   # This file
└── LICENSE                     # Project license
```

##  Technology Stack

- **Backend**: Flask (Python)
- **AI/ML**: YOLOv8 (Ultralytics), PyTorch
- **Computer Vision**: OpenCV, Pillow, dlib
- **Frontend**: HTML, CSS, JavaScript
- **Data Processing**: NumPy, Pandas

##  Model Performance

| Metric | Value |
|--------|-------|
| Face Shape Detection | 91-93% accuracy |
| Hair Type Classification | 88-92% accuracy |
| Overall mAP@0.5 | >0.89 |
| Average Inference Time | 1.8-4.2s |

##  Features Detected

- **Face Shapes**: Oval, Round, Square, Heart, Oblong
- **Hair Types**: Straight, Wavy, Curly, Coily
- **Age Categories**: Young, Mature
- **Gender**: Male, Female
- **Hair Presence**: Yes/No

##  Configuration

Edit `app.py` to customize:
```python
MAX_CONTENT_LENGTH = 16 * 1024 * 1024  # Max file size (16MB)
CONFIDENCE_THRESHOLD = 0.45  # Detection confidence threshold
MODEL_PATH = 'models/best.pt'  # Path to YOLOv8 model
```

##  API Usage

### POST `/predict`

**Request:**
- Content-Type: `multipart/form-data`
- Body: `file` (image file: PNG/JPG/JPEG, max 16MB)

**Response:**
```json
{
  "face_shape": "Oval",
  "hair_type": "Straight",
  "age_category": "Young",
  "gender": "Male",
  "confidence": 0.92,
  "primary_recommendation": {
    "name": "Sleek Undercut",
    "description": "Modern style with short sides...",
    "maintenance": "Medium"
  },
  "alternatives": [...]
}
```

##  Testing

Run automated tests:
```bash
pytest tests/
```

Run manual testing scenarios as documented in Chapter 6 of the project report.


##  Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

##  Known Limitations

- Requires clear, well-lit frontal facial photos
- Lower accuracy on heavily angled or occluded faces
- Limited to predefined hairstyle recommendations
- No real-time video analysis (planned for future)

##  Future Enhancements

- [ ] Virtual try-on with AR/generative AI
- [ ] Mobile app development (Flutter/React Native)
- [ ] Real-time video processing
- [ ] Multi-language support (Urdu, Arabic, etc.)
- [ ] Cloud deployment with auto-scaling
- [ ] User feedback loop for recommendation improvement



##  License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

##  Acknowledgments

- Dr. Ghulam Gilanie for supervision and guidance
- Department of Artificial Intelligence, IUB
- Ultralytics team for YOLOv8
- CelebA and Figaro1k dataset contributors
- Open-source community


---


⭐ If you find this project useful, please consider giving it a star on GitHub!
