# Tabulate #

[Tabulate](https://pypi.org/project/tabulate/) is a handy Python package on PyPI you can install to make fancy terminal tables.

## Install ##

With pipenv
`pipenv install tabulate`

With pip and virtualenv
`virtualenv tabulate`
`pip install tabulate --user`

## Example ##

Take a list of lists, and use tabulate to create pretty terminal tables. I created a simple file called tabulate_example.py in a dedicated venv.

```python
from tabulate import tabulate

example_list = [["Beverly Hills","California", "United States"],["Minneapolis", "Minnesota", "United States"],["Chicago","Illinois","United States"]]

print(tabulate(example_list, headers=["City","State","Country"], tablefmt="pretty"))
```

### Windows ###

`pipenv run python .\tabulate_example.py`

### Output ###

![tabulate output](/tabulate_output.png)

## Use Case ##

I recently found myself having to interact with AWS APIs and was manipulating the data structures in response and wanted to display a fairly large amount of items in my terminal.
