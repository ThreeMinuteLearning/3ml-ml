Machine learning for 3ml

Use machine learning to find the "nearest neighbours" for each story in our database using tf-idf. This can be used to provide users with a list of similar stories to the one they are reading.

# Setup

## Use virtualenv to setup python for the project

```
virtualenv ml-venv

source ./ml-venv/bin/activate

pip install jupyterlab

pip install --upgrade turicreate
```

Or use the `requirements.txt` file to avoid any dependency incompatibilities:

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

jupyter notebook
```

Use the browser to open the notebook.

# Turicreate

This is the ML library used.

- [User guide](https://apple.github.io/turicreate/docs/userguide/)
- [API docs](https://apple.github.io/turicreate/docs/api/index.html)

