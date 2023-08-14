# BEST Workshop Website Maintenance

## BEST Workshop GitHub Structure

The BEST bioinformatics workshop GitHub repository generates a [webstite](https://best-tufts.github.io/bioinformatics_workshops/) that links out to other GitHub workshop repositories and is organized into the following files/folders:

- `.github/workflows`
- `docs`
- `README.md`
- `mkdocs.yml`

### `.github/workflows`

This folder contains a file, `ci.yml`, which directs GitHub to the branch to publish. In most cases this can be left alone. However, if you create a new branch and would like the website to be generated off this branch, navigate to the `ci.yml` and change `main` to the name of the branch you have created.

### `docs`

The `docs` folder contains the following folders which add website styling and javascript:

- `images`: contains logo image for website
- `javascripts`: contains code rendering things like math equations
- `stylesheets`: contains a .css file that manually changes the website color

In this folder there are also subfolders which contain markdown documents that link out to other GitHub websites:

- `genomics`
- `transcriptomics`
- `proteomics`
- `metagenomics`

### `README.md`

The 
