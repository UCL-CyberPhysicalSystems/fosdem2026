# Setting up slides in quarto and github
The following are few steps to setup your quarto slides in github pages.

## Edit and preview slides

### Dependencies
* quarto installation (See more: https://github.com/mxochicale/tools/tree/main/quarto)
```
wget https://raw.githubusercontent.com/mxochicale/tools/refs/heads/main/quarto/download_install_quart.bash
bash download_install_quart.bash
rm download_install_quart.bash
quarto check
```

### Quarto extensions
```
quarto list extensions
quarto add quarto-ext/fontawesome
quarto remove quarto-ext/fontawesome
```

### Edit and preview slices
* Open [index.qmd](index.qmd) to edit slides. 
* Then you can preview them:
```
cd slides
quarto preview index.qmd
```


## Creating scalfolding, ci workflows, code of conduct, contributions and slides
```bash
$ tree -a
.
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── .github
│   ├── ISSUE_TEMPLATE
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   ├── pull_request_template.md
│   └── workflows
│       └── publish-quarto.yml
├── .gitignore
├── LICENSE
├── README.md
└── slides
    ├── _extensions
    │   └── quarto-ext
    │       └── fontawesome
    │           ├── assets
    │           │   ├── css
    │           │   │   ├── all.css
    │           │   │   ├── all.min.css
    │           │   │   └── latex-fontsize.css
    │           │   ├── LICENSE.txt
    │           │   └── webfonts
    │           │       ├── fa-brands-400.ttf
    │           │       ├── fa-brands-400.woff2
    │           │       ├── fa-regular-400.ttf
    │           │       ├── fa-regular-400.woff2
    │           │       ├── fa-solid-900.ttf
    │           │       ├── fa-solid-900.woff2
    │           │       ├── fa-v4compatibility.ttf
    │           │       └── fa-v4compatibility.woff2
    │           ├── _extension.yml
    │           └── fontawesome.lua
    ├── favicon.svg
    ├── figures
    │   ├── 00_template-vector-images
    │   │   └── drawing-v00.svg
    │   └── mx.svg
    ├── index.qmd
    ├── _quarto.yml
    ├── README.md
```

## Commit and upload slides
* [1/3] first commit
```bash
git add .
git commit -m ':fire: 1st commit: adds scalfolding for slides #1'
git branch -M main
git push -u origin main
```

* [2/3] Create gh-pages branch
```bash
git checkout --orphan gh-pages 
#An orphan branch is not connected to the other branches and commits, and its working tree has no files at all. 
#See [here](https://git-scm.com/docs/git-checkout) for more info.
git reset --hard
git commit --allow-empty -m "Initializing gh-pages branch"
git push origin gh-pages
git checkout main
#https://jiafulow.github.io/blog/2020/07/09/create-gh-pages-branch-in-existing-repo/
```
See [hash for template](https://github.com/UCL-CyberPhysicalSystems/fosdem2026/commit/TOADD)

* [3/3] Go to [PAGES](https://github.com/UCL-CyberPhysicalSystems/fosdem2026/settings/pages) and select in the menu `Deploy from a branch` and select gh-pages

### Push changes and publish slides
* add `feature_branch` name to [publish-quarto.yml](../.github/workflows/publish-quarto.yml)
```bash
git add .
git commmit -m '<add message> CI #ISSUE_NUMBER'
git push origin <feature_branch>
```

## References
* https://quarto.org/docs/presentations/revealjs/
* https://quarto.org/docs/presentations/revealjs/advanced.html

