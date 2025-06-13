# MCQ Generator Back-End

This is the backend API for the Multiple Choice Question (MCQ) generator project. It uses Python and machine learning models to generate questions, answers, and distractors from your input text. The backend powers the Angular front end and handles all the heavy lifting for quiz creation.

## 🚀 Getting Started

**1. (Optional) Create a virtual environment:**
This keeps your Python packages organized and avoids conflicts.

```bash
python -m venv venv
```

Activate it:

- On Windows:

```bash
.\venv\Scripts\activate
```

- On Mac/Linux:

```bash
source venv/bin/activate
```


**2. Install dependencies:**

```bash
pip install -r requirements.txt
```

**3. Download ML model checkpoints:**
Download the following models and place them in the correct folders:

- **multitask-qg-ag** (for question and answer generation):
[Download multitask-qg-ag](https://drive.google.com/file/d/1-vqF9olcYOT1hk4HgNSYEdRORq-OD5CF/view)
Place in:
    - `app/ml_models/question_generation/models/`
    - `app/ml_models/answer_generation/models/`
- **race-distractors** (for distractor generation):
[Download race-distractors](https://drive.google.com/file/d/1jKdcbc_cPkOnjhDoX4jMjljMkboF-5Jv/view)
Place in:
    - `app/ml_models/distractor_generation/models/`
- **sense2vec** (for sense2vec distractor generation):
[Download sense2vec](https://github.com/explosion/sense2vec/releases/download/v1.0.0/s2v_reddit_2015_md.tar.gz)
Extract and put the `s2v_old` folder in:
    - `app/ml_models/sense2vec_distractor_generation/models/`

**4. Run the API:**

```bash
python gay.py
```

Now your backend is live and ready to connect with the front end!

## 🧑‍💻 Examples

- If you POST a paragraph of text to the API, it will return generated MCQs with answers and distractors.
- When the Angular front end sends a request, this backend does all the question generation and sends the results back.
