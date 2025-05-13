# 🌌 Word Embedding with Star Wars Text 

## 📄 Project Description

This project implements a Word2Vec-based word embedding system using Python and Gensim to explore semantic relationships between words in the **Star Wars universe**. The model is trained on a curated dataset of Star Wars text including:

- A descriptive article summarizing all nine Star Wars movies
- Full movie scripts for Episode IV: A New Hope, Episode V: The Empire Strikes Back, and Episode VI: Return of the Jedi
- Opening crawl text from all nine Star Wars episodes

These text files were combined into one dataset and preprocessed using **NLTK** for sentence and word tokenization, stopword removal, and text cleaning.

---

## 🎯 Objective

- Preprocess natural language Star Wars text
- Train a Word2Vec model using the **Skip-Gram** architecture
- Choose 10 meaningful word pairs
- Calculate **cosine similarity** between each pair
- Identify the pair with the highest semantic similarity
- Visualize the results using a bar chart

---

## 🧠 Why Skip-Gram?

The Skip-Gram architecture (`sg=1`) was selected because it performs better on smaller or domain-specific datasets. Since Star Wars vocabulary is unique and the dataset size is moderate, Skip-Gram provides more accurate representations for rare but important terms such as "jedi", "sith", and "rebellion".

---

## 📊 Results Summary

The trained model learned a vocabulary of **6,583 unique words**. Cosine similarity was calculated for 10 Star Wars word pairs:

- The highest similarity was between **"clone" and "stormtrooper"** with a score of **0.9974**
- Other high-scoring pairs included:
  - `"hope"` & `"freedom"` → 0.9963
  - `"empire"` & `"rebellion"` → 0.9960
  - `"anakin"` & `"sith"` → 0.9953
- The lowest similarity, still relevant, was between `"death"` & `"destruction"` → 0.7766
- The model also confirmed that **"force"** is closely associated with **"jedi"** and **"skywalker"**, and the top 10 most similar words to `"sith"` included `"power"`, `"palpatine"`, `"anakin"`, and `"kenobi"`

A bar chart was created to visualize the similarity scores of all ten word pairs, clearly showing which concepts are most related in the Star Wars dataset.

---

## 📂 Files Included

- `main.py` – contains the full source code for loading, preprocessing, training, analyzing, and visualizing the Word2Vec model.
- `textFiles/` – folder containing all `.txt` files used as input data.

---

## 🚀 How to Run

1. Install dependencies:

```bash
pip install nltk gensim matplotlib
````

2. Download necessary NLTK resources inside your script or Python shell:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

3. Run the main script:

```bash
python main.py
```

The script will:

* Load all `.txt` files from the `textFiles/` folder
* Preprocess the text
* Train the Word2Vec model
* Analyze 10 Star Wars word pairs
* Display a bar chart of similarity scores

---

## 📎 References

* Gensim Word2Vec Documentation: [https://radimrehurek.com/gensim/models/word2vec.html](https://radimrehurek.com/gensim/models/word2vec.html)
* NLTK Tokenizers: [https://www.nltk.org/](https://www.nltk.org/)

---





