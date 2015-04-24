pypi-stats
==========

Get stats on some PyPI packages.

## Requirements

- Python 3 (for fun)
- beautifulsoup4 (`conda install beautiful-soup` or
  `pip install beautifulsoup4`)
- jinja2 (for `render` script)

## Example

To download package data for all packages with classifier `Topic ::
Scientific/Engineering :: Astronomy`:

```
query-pypi 387
```

To find the numerical code for your classifier of interest go to
PyPI's "browse" page (https://pypi.python.org/pypi?%3Aaction=browse),
browse to the classifier you want, and look at the 'c=' query in the
URL.

Package data is downloaded to a `data` directory, e.g.,
`data/astropy.json`.

## Render

```
render
```

Places HTML output in `output` directory.