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

## Authentication

For the GitHub API, the script requires authentication for rate-limit
reasons. There are two ways to do this:

1. Requests will by default try to read your github user name and password
   from a `~/.netrc` file. Add a line like
   ```
   machine api.github.com login USERNAME password PASSWORD
   ```
   where USERNAME and PASSWORD are your GitHub username and password.

2. Go to https://github.com/settings/tokens and generate a
   personal access token. Copy it and put it in a `GH_TOKEN` environment
   variable. Use this method if you have 2-factor authentication (2FA)
   set up. An entry in `~/.netrc` (as above) seems to conflict with this
   method so make sure to not use both.

## Deploy

To deploy built page to http://username.github.io/astrocodes, run

```
deploy.sh username
```

(uses SSH authentication with git:// protocol).
