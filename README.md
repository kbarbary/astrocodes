Astro Code Stats
================

![Astro Hack Week](https://img.shields.io/badge/Astro-Hack%20Week-green.svg?style=flat-square) *Work in progress!*

Current built page: http://kbarbary.github.io/astrocodes

Get stats on:

- Codes listed on ASCL.net
- PyPI packages with classifier `Topic ::Scientific/Engineering :: Astronomy`
  or with "astro" or "cosmo" in the description.

## Requirements

- Python 3
- requests
- beautifulsoup4 (`conda install beautiful-soup` or
  `pip install beautifulsoup4`)
- jinja2 (for `render` script)

## Run

```
astrocodes
```

Output HTML is placed in `output` directory. Data is cached in `data`
directory. (Directories are automatically created.)

## Deploy

To deploy built page to http://username.github.io/astrocodes, run

```
deploy.sh username
```

(uses SSH authentication with git:// protocol).
