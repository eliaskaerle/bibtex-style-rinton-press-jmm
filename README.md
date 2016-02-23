# Bibtex Style for Rinton Press' Journal of Mobile Multimedia

Rinton Press requires a bibliography style for it's "Journal of Mobile Multimedia" which is not compatible with any of the latex bibliography styles mentioned in [1]. In the JMM latex template available on the website [2], there is no .bst file and the bibliography is created by *begin{thebibliography}...* and then filled with *bibitem*.

**Excerpt from the documentation:**
> References are to be listed in the order cited in the text. For each cited work, include all the authors' names, year of the work, title, place where the work appears. Use the style shown in the following examples. For journal names, use the standard abbreviations. Typeset references in 9pt Times Roman.

![Bibliography Example](https://github.com/eliaskaerle/bibtex-style-rinton-press-jmm/blob/master/bib-example.jpg)

![Citation Example](https://github.com/eliaskaerle/bibtex-style-rinton-press-jmm/blob/master/cite-example.jpg)

To be independent from fixed bibliography styles and to use a .bib file, this repository provides the necessary .bst file to style the bibliography according to the Rinton Press JMM requirements and the .dbj file to change stylings and rebuilt the .bst file.

## Content
 * **rinton-press-jmm.dbj:** contains all commands for styling the citations and the bibliography, in a readable and well commented format. This file gets compiled to the actual .bst file.
 * **rinton-press-jmm.bst:** is the file actually used by latex to retrieve the styling information from.

## Usage
### Usage "as is"
To use the bibliography style "as is" copy the .bst file into your latex folder and import it by adding the two lines to your (main) .tex file:
>  \bibliographystyle{rinton-press-jmm}  
>  \bibliography{yourbibfile}

### Change styles and rebuild
To change the bibliography styles, first edit the .dbj file as described in [3] then call
> latex rinton-press-jmm.dbj

on your command line to create a new .bst file.

## Where does the dbj file come from?
The .dbj file is the output of *latex makebst* (see [4]).

## Questions? Comments? Improvements?
I would be happy to further improve that bibliography style (see [Issues](https://github.com/eliaskaerle/bibtex-style-rinton-press-jmm/issues)). Please use Github's *Issue* and *Pull Request* functions for comments and improvements on that file.

## References
[1] https://www.sharelatex.com/learn/Bibtex_bibliography_styles  
[2] http://www.rintonpress.com/style/index.html  
[3] http://www.ctex.org/documents/packages/bibref/makebst.pdf  
[4] http://tex.stackexchange.com/questions/96174/is-there-an-easy-way-to-create-or-personalize-bst-files
