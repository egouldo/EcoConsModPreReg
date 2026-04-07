# `EcoConsModPreReg` Format: A Quarto Template for Adaptive Preregistration of Ecological Models

[![](https://zenodo.org/badge/914660247.svg)](https://doi.org/10.5281/zenodo.15655052)


This repository provides the Quarto template extension for preregistering ecological modelling studies[^readme-1]. The template has been developped for use within an *Adaptive Preregistration* approach[^readme-2], however can be used with standard approaches to preregistration. For non-trivial modelling studies, especially where model parameter and structure is in any way data-contingent, we recommend following the Adaptive Preregistration procedure, which is set out at <https://egouldo.github.io/EcoConsPreReg/>[^readme-3].

[^readme-1]: This template is derived from Gould, E., Jones, C.S., Yen, J.D.L., Fraser, H.S., Wootton, H., Good, M.K., Duncan, D.H., Wintle, B.C., Rumpff, L. (2026). EcoConsPreReg: A Guide to Adaptive Preregistration for Model-Based Research in Ecology and Conservation (v1.0.2). Zenodo. <https://doi.org/10.5281/zenodo.10884635>

[^readme-2]: Gould, E., Jones, C., Yen, J., Fraser, H., Wootton, H., Good, M., Duncan, D., Hauser, C., Wintle, B., & Rumpff, L. (2025). “But I can’t preregister my research”: Improving the reproducibility and transparency of ecology and conservation with adaptive preregistration for model-based research. EcoEvoArXiv [Preprint]. <https://doi.org/10.32942/X2GW66>

[^readme-3]: Gould, E., Jones, Christopher, S., Yen, J. D. L., Fraser, Hannah, S., Wootton, H., Vivian, L., Good, M., Duncan, David, H., Rumpff, L., & Fidler, F. (2026). EcoConsPreReg: A Guide to Adaptive Preregistration for Model-Based Research in Ecology and Conservation. Zenodo. <https://doi.org/10.5281/zenodo.19064144>

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

# Referencing this work

To cite the Quarto extension "EcoConsModPreReg" in publications or preregistrations use:

> Gould, E. (2026) "EcoConsModPreReg: A Quarto Template for Preregistering Ecological Modelling Studies" Zenodo. <https://doi.org/10.5281/zenodo.15655052>

To cite the preregistration template used in "EcoConsModPreReg" in publications or preregistrations use:

> Gould, E., Jones, C., Yen, J., Fraser, H., Wootton, H., Good, M., Duncan, D., Hauser, C., Wintle, B., & Rumpff, L. (2025). “But I can’t preregister my research”: Improving the reproducibility and transparency of ecology and conservation with adaptive preregistration for model-based research. EcoEvoArXiv [Preprint]. <https://doi.org/10.32942/X2GW66>
