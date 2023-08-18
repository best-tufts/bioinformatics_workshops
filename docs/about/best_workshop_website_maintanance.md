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

This file is the GitHub facing document (not rendered on the website).

### `mkdocs.yml`

This file is used to pull in neat mkdocs features and to organize website navigation. If you are curious about how to add features to the website check out the [MkDocs Documentation Page](https://squidfunk.github.io/mkdocs-material/reference/admonitions/). This documentation will show you how to edit the yml file to add features. 

To change navigation, edit the following section of the [`mkdocs.yml`](../../mkdocs.yml) file:

```
nav:
    - About : 
        - Introduction: index.md
    - Genomics:
        - Genomics Tutorials: genomics/genomics.md
    - Transcriptomics:
        - Transcriptomics Tutorials: transcriptomics/transcriptomics.md
    - Proteomics:
        - Proteomics Tutorials: proteomics/proteomics.md
    - Metagenomics:
        - Metagenomics Tutorials: metagenomics/metagenomics.md
```

The navigation is broken down into a few headers (About, Genomics, Transcriptomics, etc.). Under the headers are markdown documents that make up the website content. the text before the `:` is the text displayed on the website sidebar. The path afterwards, is the path to the markdown document after the `docs` folder. 


## Make a New Workshop

To make a new workshop:

1. Click "New" under the repositories header on GitHub.com
2. Now click "Import A Repository"
3. Where it says "Your old repository's clone URL*" enter the following link: https://github.com/best-tufts/template
4. In the "Repository name*" field, give your new workshop a name reflective of the material it will cover
5. Click "Begin Import"
6. Go to "Settings" and click "Actions" and then select "Allow all actions and reusable workflows"
7. Now edit the `repo_url:`  line in the `mkdocs.yml` file so that it reads `repo_url: https://github.com/best-tufts/NEW_NAME_OF_REPO`
8. Edit the README.md file to include your workshop title, learning objectives and workshop website.
9. In the folder `docs/workshop_materials` create your markdown documents with workshop content. For more information on how to create a markdown document check out [GitHub's markdown documention](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
10. Once your content has been created you can render these markdown documents as webpages by editing the `nav` section in the `mkdocs.yml` file to include these new documents.
11. Give your workshop website 10 minutes to be build and deployed. Then go to "Settings" and then "Pages" where you should see the link to your new workshop website!
