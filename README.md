# Alaska Data Management User Guide source files

This directory contains the source data for the [Alaska Data Management User Guide](https://hmaier-fws.github.io/ak-dm-userguide). The site is rendered by the `quarto render` command with the compiled HTML being written to the **docs** directory.

## index.md files

The default behavior of [Quarto](https://quarto.org) is to [not render index.md files](https://quarto.org/docs/websites/#render-targets). We can change that, but I am inclined to retain that function, allowing us to maintain developer documentation within the file structure

For example, **this file** (readme.md) is not rendered, but the index.md file is!

# Contents

This directory contains several files that control the rendering of the website. The following files should not be edited:

## .quarto (directory)

Some Quarto stuff. Don't really know what's in here.

## .nojekyll

Prevents the default rendering of GitHub pages using [Jekyll](https://jekyllrb.com/)

## _quarto.yml

Site-wide configuration parameters for [Quarto](https://quarto.org)

