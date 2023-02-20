# nlp-specialization---coursera-deeplearning.ai
Natural Language Processing Specialization - Coursera/Deeplearning.ai

## Creating python environment

Install Anaconda from https://www.anaconda.com/products/distribution

```
conda create -n coursera_nlp python=3.9
conda activate coursera_nlp
```

In order to find dependencies for Python environment, clone some popular Github repos from others who have taken the course.

```bash
git clone git@github.com:amanjeetsahu/Natural-Language-Processing-Specialization.git
# alternatives
# git clone git@github.com:ibrahimjelliti/Deeplearning.ai-Natural-Language-Processing-Specialization.git
# git clone git@github.com:amanchadha/coursera-natural-language-processing-specialization.git
# search all notebooks and py files for import statements
find ./ -name *.py -o -name *.ipynb -print0 | xargs -0 egrep -sh '^\s*"import.*' | sed 's:#.*$::g' | sed 's/[[:space:]]*$//g' | sort | uniq
```

    "import ast\n",
    "import base64\n",
    "import emoji\n",
    "import functools\n",
    "import gensim\n",
    "import gin\n",
    "import itertools\n",
    "import jax\n",
    "import json\n",
    "import math
    ...

```bash
# after a bit of manual curation and removal of python provided libraries left with this
conda install gensim jax matplotlib nltk numpy pandas sacrebleu scipy sentencepiece scikit-learn
# now install some libraries that I like
conda install pytest
conda install -c conda-forge seaborn spacy jupytext jupyterlab
```

Not yet sure if I'll need these:

```bash
# nltk setup
python -m nltk.downloader popular
# spacy setup
python -m spacy download en_core_web_trf
python -m spacy download en_core_web_sm
```

### Course 1: Natural Language Processing with Classification and Vector Spaces

Lecture notes available at https://community.deeplearning.ai/t/nlp-course-1-lecture-notes/64244 (required free account through link https://community.deeplearning.ai/invites/YaM2nrk6Xx#!)

[Slides](/course_1_nlp_with_classification_and_vector_spaces/slides) from each week are available.

#### Week 1: Sentiment Analysis with Logistic Regression

* [Lab 1 - Natural Language preprocessing](course_1_nlp_with_classification_and_vector_spaces/week_1_sentiment_analysis_with_logistic_regression/c1_w1_lab1_preprocessing.md)
* [Lab 2 - Visualizing word frequencies](course_1_nlp_with_classification_and_vector_spaces/week_1_sentiment_analysis_with_logistic_regression/c1_w1_lab2_visualization.md)
* [Lab 3 - Visualizing tweets and Logistic Regression models](course_1_nlp_with_classification_and_vector_spaces/week_1_sentiment_analysis_with_logistic_regression/c1_w1_lab3_tweets_and_lr.md)
* [Assignment 1](course_1_nlp_with_classification_and_vector_spaces/week_1_sentiment_analysis_with_logistic_regression/assignment_1_logistic_regression.md)
* Assignment 1 Solution

#### Week 2: Sentiment Analysis with Naïve Bayes

#### Week 3: Vector Space Models

#### Week 4: Machine Translation and Document Search



lab_1_natural_language_preprocessing
lab_2_visualizing_word_frequencies
lab_3_visualizing_tweets_and_logistic_regression_models


Path to copy to
/Users/seth/Projects/nlp-specialization---coursera-deeplearning.ai/course_1_nlp_with_classification_and_vector_spaces/week_1_sentiment_analysis_with_logistic_regression/