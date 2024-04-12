# Alaska Data Management User Guide source files

This directory contains the source data for the [Alaska Data Management User Guide](https://hmaier-fws.github.io/ak-dm-userguide). The site is rendered by the `quarto render` command with the compiled HTML being written to the **docs** directory.

## README.md files

The default behavior of [Quarto](https://quarto.org) is to [not render README.md files](https://quarto.org/docs/websites/#render-targets). We can change that, but I am inclined to retain that function, allowing us to maintain developer documentation within the file structure

For example, **this file** is not rendered, but the index.md file is!
