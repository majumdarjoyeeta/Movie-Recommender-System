🎥🍿 Movie Recommender System 📽️✨
Collaborative Filtering Based Movie Recommendation Engine

🔗 GitHub Repo: majumdarjoyeeta/-Movie-Recommender-System

📁 Dataset
This project uses the famous MovieLens 100k dataset 🎞️ from GroupLens with:

📄 u.data — user ratings (👤 user_id, 🎬 item_id, ⭐ rating, ⏱️ timestamp)

🎟️ Movie_titles — movie ID to title mapping

🧰 Libraries Used
🐼 pandas — data manipulation

🔢 numpy — numerical operations

📊 matplotlib, 🎨 seaborn — (optional) for data visualization

🔍 Data Exploration
We start by loading the user ratings data:

python
Copy
Edit
pd.read_csv('u.data', sep='\t', names=['user_id', 'item_id', 'rating', 'timestamp'])
Example output 👇

user_id	item_id	rating	timestamp
0	50	5	881250949
Then we merge it with the movie titles 🎬 to get readable names instead of just IDs.

🛠️ How It Works
🔄 1. Preprocessing
🎛️ Created a user-movie rating matrix

🧹 Cleaned and structured data

📊 2. Movie Statistics
Calculated:

🧮 Total Ratings per Movie

📈 Average Rating per Movie

python
Copy
Edit
ratings_mean_count_df = pd.concat([ratings_count_df, ratings_mean_df], axis=1)
🎯 3. Recommendations Engine
We picked "Titanic (1997)" 🚢 as our base movie to recommend similar ones!

Using correlation-based collaborative filtering, we find movies users often rate similarly:

python
Copy
Edit
titanic = userid_movietitle_matrix['Titanic (1997)']
✅ Filtered for movies with at least 80+ ratings for reliability.

📌 Top 5 Movies similar to Titanic:

🎬 Movie	🔗 Correlation	🧾 Count
Titanic (1997)	1.00	350
River Wild, The (1994)	0.50	146
Abyss, The (1989)	0.47	151
Bram Stoker's Dracula (1992)	0.44	120
True Lies (1994)	0.43	208
💡 Possible Improvements
Add 🎭 genre filtering

Integrate 🧠 matrix factorization or deep learning

Create a 🖥️ Streamlit / Flask UI

📌 Project Link
🔗 GitHub Repository:
👉 [https://github.com/majumdarjoyeeta/-Movie-Recommender-System](https://github.com/majumdarjoyeeta/-
