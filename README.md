Machine learning for 3ml

Use machine learning to find the "nearest neighbours" for each story in our database using tf-idf. This can be used to provide users with a list of similar stories to the one they are reading.

# Setup

## Use venv to setup python for the project

```
$ python -m venv ./venv
$ source ./venv/bin/activate(.fish)
$ pip install jupyterlab scikit-learn pandas nltk
```

Or use the requirements file (created using `pip freeze`) if you have problems:
```
pip install -r requirements.txt
```

# Extract story data as a CSV file

Dump the stories table to `stories.csv`:

```
psql --csv -d my3ml -o stories.csv -c 'select id,title,content from story'
```

# Running the notebook

```
source ./ml-venv/bin/activate

jupyter-lab 3ml_stories.ipynb
```

Use the browser to open the notebook.

