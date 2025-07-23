GitHub Actions for Pandoc
=========================

This repository offers GitHub Actions to facilitate the use of
pandoc on that platform.

QUAT: this fork [disables man-db triggers](https://askubuntu.com/questions/272248/processing-triggers-for-man-db) on ubuntu runners, since it takes a long time and i won't be needing those man pages anyway. Please only use if you're me, i don't think this is ready to upstream 

## `pandoc/actions/setup`

This actions installs pandoc in the current runner. The `version` parameter
allows to install a specific version. The default is to install the latest
version.

### Example

```
jobs:
  pandoc:
    steps:
      - name: Install pandoc
        uses: pandoc/actions/setup@v1

      - name: Run pandoc
        run: pandoc --version
```
