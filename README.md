# Netflix Recommendation System

### Introduction
This project implements a content-based recommendation system for Netflix titles. It suggests similar movies or TV shows based on a user's input, using features such as title, director, cast, genre, and description.
### Features

- Content-based filtering for movie and TV show recommendations
- Web interface for easy user interaction
- Scalable design that can handle large datasets
- Utilizes natural language processing techniques for better recommendations

### Requirements

- Python 3.7+
- pandas
- scikit-learn
- Flask
- numpy

### Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/netflix-recommendation-system.git
cd netflix-recommendation-system
```
2. Install the required packages:
```python
pip install -r requirements.txt
```
3. Download the Netflix titles dataset (netflix_titles.csv) and place it in the project root directory.

###Usage

1. Start the Flask server: `python app.py`
2. Open a web browser and navigate to `http://localhost:5000`
3. Enter a Netflix title in the search box and click "Get Recommendations" to see similar titles.

### How It Works

1. Data Processing: The system loads and cleans data from the Netflix titles CSV file.
2. Feature Engineering: It creates a 'soup' of features for each title, combining elements like title, director, cast, genres, and description.
3. Vectorization: The text data is converted into numerical vectors using CountVectorizer.
4. Similarity Calculation: Cosine similarity is applied to these vectors to quantify how similar each title is to every other title.
5. Recommendation: When a user inputs a title, the system finds the most similar titles based on the cosine similarity scores.

### File Structure

- ***app.py:*** Main Flask application
- ***content_based_nrc.py:*** Core recommendation system logic
- ***templates/:*** HTML templates for the web interface
- ***netflix_titles.csv:*** Dataset of Netflix titles (not included in repo)
- ***requirements.txt:*** List of Python dependencies
