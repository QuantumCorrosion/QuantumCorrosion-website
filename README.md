# quantumcorrosion.github.io

This is the GitHub repository for the quantumcorrosion.github.io website. 
It uses the HUGO static site builder, along with a customised version of the
Academic theme/framework. 

## Updating the website

This website uses the static-site generator Hugo. 

This repository store the Markdown formatted text file which define the
website. 

Hugo is then invoked to render these text files to the generated HTML/CSS,
which sits in the `public` sub folder. 
This is also a git repository, pointing to a special 'github pages' repository
which is then served by GitHub as HTML.

## Domain name

http://quantumcorrosion.org is registered for 5 years from NameCheap starting on 18th April 2018.

## Setting up a local machine

1) Clone this repository, which contains the human-readable Markdown for the website.

`git clone --recursive git@github.com:QuantumCorrosion/QuantumCorrosion-website.git `

The recursive flag is used to initialise submodules; in this case that means the "academic theme" used to create the site (essentially a template).

2) Acquire Hugo. `Go` programs are distributed as statically compiled executables, so this should be a simple matter of downloading the relevant binary, and placing the `hugo` executable somewhere in your path, such as `~/bin`. 

Hugo releases: https://github.com/gohugoio/hugo/releases

The extended version is needed. To figure out the release version needed read "min\_version" from the file "themes/academic/theme.toml" (path relative to THIS repository).

3) Enter this repository, and clone the 'github-pages' HTML-repository (`quantumcorrosion.github.io`) to a folder named `public`

```
cd QuantumCorrosion-website
mkdir public
git clone git@github.com:QuantumCorrosion/quantumcorrosion.github.io.git ./public
```

You should now have a complete version-controlled copy of the website, scripts to build the HTML, and a version-controlled copy of the 'github-pages' website itself (`./public`).

## Workflow

* `update_academic.sh` will update / instantiate a copy the academic theme used to compile the website. Updating the theme could result in breakages, as the expected formatting changes. 

* `live_serve.sh` will run Hugo automatically when Markdown files are updated, and serve them locally to your web browser. You should use this as you make edits to the website, to check that things render correctly. 

* Once you are happy with the local version of the website, `build_site.sh` will render the Markdown to HTML into the /public folder. 

* You should then check-in changes to the Markdown / backend of the site, and then enter the `/public` directory and commit and push changes there. A few minutes later the changes will be live.

A typical workflow will look like:-

```
. live_serve.sh &
(edits .md files in /content/ etc.)
git add content/*/*.md
git commit
git push

. build_site.sh
cd public
git add -a
git commit
git push
```
