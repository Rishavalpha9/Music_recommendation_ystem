# 🎵 Music Recommendation System

A content-based music recommendation system that suggests similar songs based on lyrics similarity using Natural Language Processing (NLP) and Machine Learning.

![Music Recommendation System](https://via.placeholder.com/800x400.png?text=Music+Recommendation+System+Dashboard)

## ✨ Features

- **Lyrics-based Recommendations**: Find songs with similar lyrical content
- **Modern Web Interface**: Clean, responsive design with intuitive UI
- **Fast Performance**: Pre-computed similarity matrix for instant results
- **Smart Search**: Case-insensitive search with autocomplete
- **Detailed Song Information**: View artist and song details for each recommendation

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- pip (Python package manager)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/music-recommendation-system.git
   cd music-recommendation-system
   ```

2. **Set up a virtual environment**:
   ```bash
   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate

   # On Windows
   python -m venv venv
   .\venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download NLTK data**:
   ```bash
   python -c "import nltk; nltk.download('punkt')"
   ```

## 📂 Data Preparation

1. Download the song lyrics dataset (e.g., from [Kaggle](https://www.kaggle.com/mousehead/songlyrics))
2. Place the CSV file in the `data` directory
3. (Optional) Update the `SONG_DATA_FILE` in `process_data.py` if needed

## 🏃‍♂️ Running the Application

1. **Process the data and train the model**:
   ```bash
   python process_data.py
   ```

2. **Start the Flask development server**:
   ```bash
   python app.py
   ```

3. **Open your web browser** and navigate to:
   ```
   http://localhost:5000
   ```

## 🏗️ Project Structure

```
music-recommendation-system/
├── app.py                # Flask application
├── process_data.py       # Data processing and model training
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables
├── .gitignore            # Git ignore file
├── README.md             # This file
├── data/                 # Directory for song data
│   └── songdata.csv      # Song lyrics dataset
├── models/               # Directory for trained models
│   ├── df.pkl           # Processed dataset
│   └── similarity.pkl   # Precomputed similarity matrix
└── templates/            # HTML templates
    ├── index.html       # Main page
    └── error.html       # Error page
```

## 🧠 How It Works

### Text Processing
- Converts text to lowercase
- Removes special characters and numbers
- Tokenization and stemming using NLTK

### Feature Extraction
- Uses TF-IDF (Term Frequency-Inverse Document Frequency) to convert lyrics into numerical features
- Considers both unigrams and bigrams for better context understanding

### Similarity Calculation
- Computes cosine similarity between all pairs of songs
- Pre-computes the similarity matrix for faster recommendations

### Web Interface
- Built with Flask for the backend
- Responsive frontend using Bootstrap 5
- Interactive UI with loading states and animations

## 📊 Model Performance

- **Preprocessing Time**: ~5-10 minutes for 10,000 songs
- **Recommendation Speed**: < 100ms per request
- **Memory Usage**: ~500MB for 10,000 songs

## 🧪 Testing

Run the test script to verify the API endpoints:

```bash
python test_api.py
```

## 🌐 Deployment

### Heroku Deployment

1. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
2. Run the deployment script:
   ```bash
   chmod +x deploy.sh
   ./deploy.sh
   ```

### Docker Deployment

```bash
# Build the Docker image
docker build -t music-recommendation .

# Run the container
docker run -p 5000:5000 music-recommendation
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Dataset: [Song Lyrics from 6 Modern Artists](https://www.kaggle.com/mousehead/songlyrics)
- Built with Flask, scikit-learn, and NLTK
- Inspired by content-based recommendation systems

---

<div align="center">
  Made with ❤️ by Abhi Suryawanshi
</div>
FAQ: Include a FAQ section for common issues
📝 Notes
Make sure to replace placeholder values (like yourusername and Your Name) with your actual information
Update the performance metrics based on your actual testing
Add any additional features or customizations specific to your implementation
