📚 Book Recommender System: An End-to-End Machine Learning Project
📖 Project Overview
This repository contains an end-to-end Machine Learning project designed to suggest personalized book recommendations. The system leverages two distinct recommendation approaches and is served through a user-friendly Flask web application, allowing users to discover new books based on popularity or specific titles they enjoy.

The core of this project is built upon the Book-Crossing dataset, a classic set of tables containing information about 270,000+ books, 1.1 million+ ratings, and 278,000+ users.

⭐ Key Features
Popularity-Based Recommender: Displays the top 50 books with the highest average ratings on the platform, filtered to ensure a minimum number of votes (at least 250 ratings) for reliable suggestions.

Collaborative Filtering Recommender: Suggests 5 similar books based on a user-provided title. This uses an Item-Item approach, calculating the Cosine Similarity between different books based on the collective rating patterns of experienced users.

Flask Web UI: A simple and intuitive dark-themed web interface for browsing popular books and searching for recommendations.

🛠️ Tech Stack & Prerequisites
Language: Python 3.9+

Machine Learning / Data Processing: Jupyter Notebook, NumPy, Pandas, Scikit-Learn (specifically cosine_similarity)

Web Framework: Flask

Frontend: HTML, CSS, Bootstrap

You will need to have Python and pip installed on your machine before running this project.

🚀 Getting Started: Installation & Usage
Follow these steps to set up and run the Book Recommender System locally.

1. Clone the Repository
Bash
git clone https://github.com/HMBadgujar/Book-Recommender.git
cd Book-Recommender
2. Set Up a Virtual Environment (Recommended)
This helps keep your dependencies isolated.

Bash
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate
3. Install Required Dependencies
Bash
pip install -r requirements.txt
(Note: The requirements.txt file includes flask, gunicorn, numpy, pandas, scikit-learn, and pickle5.)

4. Run the Flask Application
Bash
python app.py
After the server starts, open your web browser and navigate to:
http://127.0.0.1:5000/

5. Using the Recommender
Home Page: Browse the Top 50 Books grid, featuring cover images, titles, and average ratings.

Recommend Page:

Click the "Recommend" link in the navigation bar.

Enter the exact title of a popular book (e.g., "The Da Vinci Code," "1984," or "Harry Potter and the Chamber of Secrets").

Click "Submit."

The system will generate and display 5 recommended books that have similar voting patterns.

(Note: The system is trained on specific books that met a minimum popularity threshold, so it will only be able to recommend based on titles it "knows" from the cleaned dataset.)

📊 Dataset Information
The project uses the Book-Crossing Dataset, which consists of three files:

Books.csv: Contains details about books (ISBN, Title, Author, Year, Publisher, and Image URLs).

Users.csv: Contains user profiles (User-ID, Location, Age).

Ratings.csv: Contains book ratings, provided by users to specific books (User-ID, ISBN, Book-Rating from 0-10).
