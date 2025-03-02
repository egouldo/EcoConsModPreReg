# `EcoConsModPreReg` Format: A Quarto Template for Adaptive Preregistration of Ecological Models

Here we present a preregistration template for ecological models in ecology, conservation and related fields. This template is based on the EcoConsPreReg: A Guide to Adaptive Preregistration for Model-Based Research in Ecology and Conservation (v1.0.2) by Gould *et al.* (2024)[^1].

## Installation

```bash
quarto use template egouldo/EcoConsModPreReg
```

This will install the extension and create an example qmd file containing the EcoConsPreReg template that you can use as a starting place for your preregistration. The template source code is located here: [template.qmd](template.qmd).

## Usage

For non-trivial modelling studies, especially where model parameter and structure is in any way data-contingent, we recommend taking an *Adaptive Preregistration* approach (insert cross-ref to preprint). Replace author, author-affiliations, keywords, title and abstract yaml metadata as relevant to your study. All preregistration items should be completed unless marked as optional, or are not applicable to your study.

## Format Options

The `EcoConsModPreReg` format can be rendered to html, pdf, or docx. `EcoConsModPreReg` documents deafult to using the Methods in Ecology and Evolution journal citation style. This can be overridden by adding your own .csl file to the document directory, and updating the document's yaml metadata to point to the new .csl file, see the [quarto citations authoring guide](https://quarto.org/docs/authoring/citations.html) for details.


Standard Quarto options are also available, and can be overridden in the document's yaml metadata, see the [quarto scholarly writing guide](https://quarto.org/docs/authoring/front-matter.html).

[^1]: Gould, E., Jones, Christopher, S., Yen, J. D. L., Fraser, Hannah, S., Wootton, H., Vivian, L., Good, M., Duncan, David, H., Rumpff, L., & Fidler, F. (2024). EcoConsPreReg: A Guide to Adaptive Preregistration for Model-Based Research in Ecology and Conservation (v1.0.2). Zenodo. https://doi.org/10.5281/zenodo.10884635
