# Tapir sapling breakage – Biotropica

This repository contains the data and reproducible R/Quarto workflows associated with the post-peer-review revision of the manuscript:

**Lowland tapirs (*Tapirus terrestris*) as ecosystem engineers: selective sapling breakage and its structural and dynamic consequences in the Yungas subtropical Andean forests of Argentina**

## Rendered workflows

Browser-ready versions of the reproducible workflows are available at:

https://andrestalamo.github.io/tapir-sapling-breakage-biotropica/

The QMD files remain the authoritative reproducible source documents; the HTML files are provided for convenient inspection without requiring R or Quarto.

## Current post-revision workflows

- `statistical_analysis_workflow_post_revision.qmd` is the authoritative workflow for the statistical analyses reported in the revised manuscript.
- `figures_workflow_post_revision_english.qmd` reproduces the manuscript's data-driven figures (excluding photographs and maps). Figure 5 obtains its p-values programmatically from the post-revision linear mixed-effects models.

Rendered, self-contained HTML versions are included for consultation without running R or Quarto:

- `statistical_analysis_workflow_post_revision.html` — rendered statistical analysis workflow.
- `figures_workflow_post_revision_english.html` — rendered figure workflow.

The QMD files remain the authoritative source documents; the HTML files are their rendered outputs.

## Required data

Both data files must be present in the repository root:

- `Renovales (3).xlsx` — sapling-level data used by the statistical and figure workflows.
- The Excel workbook whose filename ends in `Quiebres_Coberturavegetal.xlsx` — understory-cover and seasonal-breakage data used by both workflows. The workflows locate this file by its stable suffix so that Unicode normalization of the accented filename does not affect reproducibility.

## Rendering

Install [R](https://www.r-project.org/) and [Quarto](https://quarto.org/), then install the R packages loaded in each workflow. From the repository root, render the current workflows in clean R sessions with:

```sh
quarto render statistical_analysis_workflow_post_revision.qmd
quarto render figures_workflow_post_revision_english.qmd
```

Each `quarto render` invocation starts a separate R process. The workflows check for the required data and stop with an informative error if a required file is unavailable.

## Archived pre-revision workflows

The following historical workflows are retained for provenance and should not be used to reproduce the revised manuscript:

- `statistical_analysis_workflow.qmd` — pre-revision statistical workflow.
- `figures_workflow.qmd` — pre-revision figure workflow.

## Contact

Andrés Tálamo  
Email: andrestalamo@gmail.com
