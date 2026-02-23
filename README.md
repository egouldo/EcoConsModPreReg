# `EcoConsModPreReg` Format: A Quarto Template for Adaptive Preregistration of Ecological Models

[![](https://zenodo.org/badge/914660247.svg)](https://doi.org/10.5281/zenodo.15655052)

Here we present a preregistration template for ecological models in ecology, conservation and related fields. This template is based on the EcoConsPreReg: A Guide to Adaptive Preregistration for Model-Based Research in Ecology and Conservation (v1.0.2) by Gould *et al.* (2024)[^readme-1].

[^readme-1]: Gould, E., Jones, C.S., Yen, J.D.L., Fraser, H.S., Wootton, H., Good, M.K., Duncan, D.H., Wintle, B.C., Rumpff, L. (2024). EcoConsPreReg: A Guide to Adaptive Preregistration for Model-Based Research in Ecology and Conservation (v1.0.2). Zenodo. <https://doi.org/10.5281/zenodo.10884635>

For non-trivial modelling studies, especially where model parameter and structure is in any way data-contingent, we recommend taking an *Adaptive Preregistration* approach (insert cross-ref to preprint). However, this template may be used with any mode of preregistration.

## Creating a New Preregistration

``` bash
quarto use template egouldo/EcoConsModPreReg
```

This command will install the EcoConsPreReg extension in your project workspace, including a quarto template that can be used as a starting point for your preregistration. The template source code is located here: [template.qmd](template.qmd). When you execute the command you will be prompted to choose an installation location---either in the working (root) directory, or in a subdirectory (existing or new). By default, the installation will create the quarto template file `template.qmd` in the working (root) directory. If you specify a subdirectory location the installation process will rename the template file to match the name of the enclosing directory (e.g., `specified_subdirectory/specified_subdirectory.qmd`). 

## Use with Existing Preregistration Document

To use the quarto template with an existing project or document, run the following command in the terminal:

``` bash
quarto add egouldo/EcoConsModPreReg
```

# Usage

## Editing

Edit the template file: Replace author, author-affiliations, keywords, title and abstract yaml metadata as relevant to your study. All preregistration items should be completed unless marked as optional, or are not applicable to your study.

## Format Options

The `EcoConsModPreReg` format can be rendered to html, pdf, or docx. Standard Quarto formatting options are also available, and can be overridden in the document's yaml metadata, see the [quarto scholarly writing guide](https://quarto.org/docs/authoring/front-matter.html).

To use the pdf extension with an existing document, add the following in your document yaml:

``` yaml
format:
  pdf: default
    ecoconsmodprereg-pdf:
      keep-tex: true
```

### Author Affiliations

To output multiple author affiliations with footnotes when rendering to pdf, the yaml tag `affil-id:` must be provided for each author rather than using the default quarto `affiliations:` tag as for html and docx formats. This is because the pdf output uses the LaTeX `authblk` package to format author affiliations. For details, see <https://stackoverflow.com/a/76016913/4593464>.

### The CRediT taxonomy

Each listed author / contributor's intended contribution should be provided with the [CRediT taxonomy](https://credit.niso.org/). For details, see: [quarto yaml options for CRediT role values](https://quarto.org/docs/journals/authors.html#roles).

### Citations

`EcoConsModPreReg` documents default to using the [Methods in Ecology and Evolution](https://besjournals.onlinelibrary.wiley.com/hub/journal/2041210x/author-guidelines "Author Guidelines") journal citation style. This can be overridden by adding your own `.csl` file to the document directory, and updating the quarto document yaml metadata to point to the new .csl file, see the [quarto citations authoring guide](https://quarto.org/docs/authoring/citations.html) for details.
