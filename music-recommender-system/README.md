# Music Recommendation System

A machine learning-based music recommendation system that suggests similar songs based on audio features using Spotify dataset.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project implements a content-based music recommendation system that analyzes audio features of songs to find similar tracks. The system uses cosine similarity to calculate relationships between songs based on their musical characteristics.

## ✨ Features

- **Data Analysis**: Comprehensive analysis of Spotify music dataset
- **Visualization**: Interactive charts showing genre distribution, audio features, and correlations
- **Content-Based Filtering**: Recommends songs based on audio similarity
- **Artist Analysis**: Top artists by track count visualization
- **Genre Comparison**: Energy distribution analysis across different genres

## 📊 Dataset

The project uses the **Ultimate Spotify Tracks DB** dataset from Kaggle containing:
- **Source**: [Kaggle - Ultimate Spotify Tracks DB](https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db/data)
- **File**: SpotifyFeatures.csv
- **Content**:
  - Track names and artist information
  - Audio features (acousticness, danceability, energy, valence, tempo, loudness)
  - Genre classifications
  - Various musical attributes
  - 232,725+ tracks from different genres and time periods

## 🚀 Installation

1. **Clone the repository**
```bash
git clone https://github.com/hilmiozbay/recommender-systems.git
cd music-recommender-system
```

2. **Install required packages**
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook music-recommendation.ipynb
```

## 💻 Usage

1. **Load the dataset**: The notebook automatically loads the first 1000 songs from the dataset
2. **Explore the data**: Run cells to see data analysis and visualizations
3. **Get recommendations**: Use the recommendation function:

```python
# Example usage
recommendations = recommend_song("Shape of You", df, similarity_matrix, top_k=5)
print(recommendations)
```

## 🔧 How It Works

### 1. Data Preprocessing
- Load Spotify features dataset
- Select relevant audio features
- Normalize features using MinMaxScaler

### 2. Similarity Calculation
- Calculate cosine similarity matrix between all songs
- Use audio features: acousticness, danceability, energy, valence, tempo, loudness

### 3. Recommendation Generation
- Find input song in dataset
- Calculate similarity scores with all other songs
- Return top-k most similar songs

### 4. Algorithm Flow
```
Input Song → Feature Extraction → Similarity Calculation → Top-K Selection → Recommendations
```

## 📈 Results

The system provides:
- **Similar song recommendations** with similarity scores
- **Artist and genre information** for each recommendation
- **Visual analysis** of music trends and patterns
- **Feature correlation analysis** showing relationships between audio characteristics

### Sample Output
```
Recommendations for "Shape of You":
1. Song A - Artist X - Pop (Similarity: 0.95)
2. Song B - Artist Y - Pop (Similarity: 0.92)
3. Song C - Artist Z - Dance (Similarity: 0.89)
```

## 🛠 Technologies Used

- **Python 3.x**: Main programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Machine learning algorithms
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development environment

## 📁 Project Structure

```
music-recommender-system/
│
├── music-recommendation.ipynb    # Main notebook with analysis and model
├── SpotifyFeatures.csv          # Dataset file
├── README.md                    # Project documentation
└── .ipynb_checkpoints/          # Jupyter checkpoint files
```

## 🎨 Visualizations Included

- **Genre Distribution**: Bar chart of most popular music genres
- **Audio Features**: Histograms showing distribution of musical characteristics
- **Correlation Heatmap**: Relationships between different audio features
- **Genre-Energy Analysis**: Box plots comparing energy levels across genres
- **Top Artists**: Bar chart of artists with most tracks

## 🔮 Future Enhancements

- [ ] Add collaborative filtering approach
- [ ] Implement hybrid recommendation system
- [ ] Add user rating system
- [ ] Create web interface
- [ ] Include more diverse audio features
- [ ] Add playlist generation functionality

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Hilmi Özbay**
- GitHub: [@hilmiozbay](https://github.com/hilmiozbay)

## 🙏 Acknowledgments

- **Zaheen Hamidani** for providing the Ultimate Spotify Tracks DB dataset on Kaggle
- **Spotify** for the original audio features and track information
- **Kaggle** community for hosting and maintaining the dataset
- **Scikit-learn** community for machine learning tools
- Open source contributors for various libraries used

---
