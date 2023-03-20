#Web: https://annguyen0601.github.io/NCKH-front/#/

## Installation guide

### Creating a virtual environment *(optional)*
To avoid any conflicts with python packages from other projects, it is a good practice to create a [virtual environment](https://docs.python.org/3/library/venv.html) in which the packages will be installed. If you do not want to this you can skip the next commands and directly install the the requirements.txt file. 

Create a virtual environment :

    python -m venv venv

Enter the virtual environment:

*Windows:*

    . .\venv\Scripts\activate

*Linux or MacOS*

    source .\venv\Scripts\activate

### Installing packages

    pip install -r .\requirements.txt 

### Downloading data

#### Question-answer model
Download the [multitask-qg-ag model](https://drive.google.com/file/d/1-vqF9olcYOT1hk4HgNSYEdRORq-OD5CF/view?usp=sharing) checkpoint and place it in the  `app/ml_models/question_generation/models/`and `app/ml_models/answer_generation/models/`directory.

#### Distractor generation 
Download the [race-distractors model](https://drive.google.com/file/d/1jKdcbc_cPkOnjhDoX4jMjljMkboF-5Jv/view?usp=sharing) checkpoint and place it in the  `app/ml_models/distractor_generation/models/` directory.

Download [sense2vec](https://github.com/explosion/sense2vec/releases/download/v1.0.0/s2v_reddit_2015_md.tar.gz), extract it and place the `s2v_old`  folder  and place it in the `app/ml_models/sense2vec_distractor_generation/models/` directory.

*Run the API:*

    python gay.py

