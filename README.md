# ROCKYOU.AI

# 🔐 AI-Powered Password Strengthener

## 🚀 Project Overview

This tool helps users evaluate the **strength** of their passwords by comparing them against a dataset of weak or leaked passwords. It uses **AI/NLP techniques** like **TF-IDF vectorization** and similarity scoring to detect similar patterns. It also generates **stronger yet human-memorable suggestions** based on the input.

## 🧠 Features

- Accepts user-entered password
- Loads and processes a list of weak or leaked passwords
- Uses AI/NLP (TF-IDF + cosine similarity) to:
  - Find similar passwords
  - Count number of matches
- Suggests improved, strong, yet memorable alternatives
- All logic runs on **Google Colab**

## 📚 Tech Stack

- Python 3
- Google Colab (Jupyter Notebook)
- Libraries:
  - `pandas`
  - `scikit-learn` (TF-IDF, cosine similarity)
  - `nltk` (optional for tokenization/stemming)
  - `re`, `random`, `string`

## 📂 Project Structure

```
ai-password-checker/
│
├── password_checker.ipynb       # Main Colab notebook
├── weak_passwords.txt           # Dataset of known weak/leaked passwords
└── utils/
    └── password_utils.py        # Helper functions (optional modular version)
```

## ⚙️ How to Run

1. **Open in Google Colab**:
   - Upload `password_checker.ipynb` and `weak_passwords.txt` to your Colab session.

2. **Install dependencies** (Colab usually has them pre-installed):
   ```python
   !pip install -U scikit-learn
   ```

3. **Run each cell step-by-step**:
   - Upload or link your `weak_passwords.txt`
   - Enter a password (e.g., `hidden99#`)
   - View similarity results
   - See stronger suggestions like: `H1d33n99#`, `h1ddEn_99!`, etc.

## 🔒 Sample Output

```
Input Password: hidden99#
Found 7 similar weak passwords.
Suggested Stronger Versions:
- H1ddEn99#
- h1dd3n_99!
- HIDDEN_99#
```

## 💡 How It Works

- Loads all passwords from file
- Converts them into vector space using **TF-IDF**
- Measures similarity between user password and dataset
- If similar passwords found:
  - Suggests stronger alternatives using rules like:
    - Character substitution (`i` → `1`, `e` → `3`)
    - Case variation
    - Symbol addition

## 🛡️ Future Improvements

- Train ML model on password strength scoring
- Integrate zxcvbn or password entropy libraries
- Deploy as Flask or Streamlit app

## 👤 Author

- **Albin Tenny**  
  AI & Cybersecurity Enthusiast  
