# 📚 Semantic Book Recommender

An AI-powered book recommendation system that uses **semantic similarity** and **emotional tone analysis** to suggest books tailored to your preferences. Built with **LangChain**, **Gradio**, and **llm model**, the app enables users to discover books not just by genre—but by *how they feel*.

---

## 🚀 Features

- 🔍 **Semantic Search**: Find books similar to your input description using vector embeddings.
- ❤️ **Emotion-Aware Recommendations**: Filter results by tone—joy, fear, sadness, and more—using a RoBERTa-based emotion classifier.
- 🗂️ **Category Filtering**: Narrow down results based on genre or category.
- 🖼️ **Visual Gallery**: Get a gallery-style view of books with covers, titles, authors, and short blurbs.
- 💾 **Persistent Vector DB**: Uses `Chroma` to store embeddings for fast search without reprocessing.

---

## 🧠 Tech Stack

- **Gradio** – for building the interactive UI
- **LangChain** + **Chroma** – for vector DB and semantic search
- **llm model** – for embedding text into semantic vectors
- **Transformers (🤗)** – for performing emotion classification
- **Pandas / NumPy** – for data handling and transformation

---

## 📂 Dataset

- Based on the [7k Books dataset](https://www.kaggle.com/datasets)
- Core columns:
  - `title`, `description`, `authors`, `categories`
  - `average_rating`, `thumbnail`, `num_pages`, `published_year`
- Enriched with:
  - `simple_categories` (cleaned category)
  - Emotion scores: `joy`, `sadness`, `anger`, `fear`, `disgust`, `surprise`, `neutral` – using `j-hartmann/emotion-english-distilroberta-base`

---

## ✨ Example Usage

> “A coming-of-age story with themes of love and healing.”

With tone = `Sad` and category = `Romance`, the app returns 16 semantically similar books that match both the emotional tone and genre.

---

## 📸 Demo
![image](https://github.com/user-attachments/assets/f16093c4-c590-4c3c-b87f-f40c27b55b29)

![image](https://github.com/user-attachments/assets/c6c6e017-9612-4883-ac4a-41fc23e58cbe)




---

## 🛠 Future Improvements

- 🔄 Batch emotion analysis for faster preprocessing
- 🌍 Deploy on Hugging Face Spaces or Streamlit Cloud
- 📖 Add full book detail view with reviews
- 📈 Add visual EDA dashboard

---


## 📄 License

This project is licensed under the [MIT License](LICENSE).
