# Description

Template for writing math documents in LaTeX.

1. I use the TeX package `subfiles` in order to split into a main file and subfiles which can be compiled independently. The following are files and directories in the root folder of this repository: 
    * `text.tex` --- the main tex document containing the entire preamble and structure. It is a container for subfiles; these are added by `\subfile{}`.
    * `bibliography/bibliography.bib` --- bibliography in `BibLaTeX`.
    * `latex-packages/` --- TeX style files from [latex-packages](https://github.com/p135246/latex-document). The philosophy is to have a definition for every recuring mathematical construction I encounter. 
    * `graphics/` --- graphics which I draw mostly in `TikZ` and under time pressure in `Inkscape` or on my tablet.
    * `subfiles/` --- subfiles.
2. I use `git` for versioning for projects on long-term.
3. I use `gvim` with `vimtex` as editor. Here is my [dot-vim.](https://github.com/p135246/dot-vim)

# Workflow
1. Make a directory `my-new-note` and `cd` into it.
2. Inside `my-new-note` run the following command to clone this git repository and its submodules:

    ``git clone --recurse-submodule https://github.com/p135246/latex-document .``

3. `cd` into `subfiles` and run `cp subfile.tex my-first-note.tex` to create a working tex file.
4. Compile either `my-first-note` directly or add it to the list of subfiles in the main `text.tex` file.
5. If a new project is started, do not forget to initialize a `git` repository in the root folder.
