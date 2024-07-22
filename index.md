---

layout: page
title: PhysiCell
subtitle: PhysiCell Guide
hero_image: /CoGAPSGuide/images/hero.jpg
<!-- hero_height: is-fullwidth -->
hero_darken: true
show_sidebar: false
<!-- hero_link: https://github.com/FertigLab/CoGAPS
hero_link_text: GitHub Repository -->

---

# Introduction

[![downloads](https://bioconductor.org/shields/downloads/release/CoGAPS.svg)](http://bioconductor.org/packages/stats/bioc/CoGAPS/)
<!-- [![Build Status](https://travis-ci.org/FertigLab/CoGAPS.svg?branch=master)](https://travis-ci.org/FertigLab/CoGAPS) -->

<img src="images/CoGAPSLogoSmall.png" align="left" style="margin: 0px 20px 0px 0px;" />Non-negative matrix factorization (NMF) is an unsupervised learning method well suited to high-throughput biology. Still, inferring biological processes requires additional post hoc statistics and annotation for interpretation of features learned from software packages developed for NMF implementation.
<p>Here, we aim to introduce a suite of computational tools that implement NMF and provide methods for accurate, clear biological interpretation and analysis. A generalized discussion of NMF covering its benefits, limitations, and open questions in the field is followed by <strong>three procedures</strong> for the Bayesian NMF algorithm CoGAPS (Coordinated Gene Activity across Pattern Subsets). Each procedure will demonstrate NMF analysis to quantify cell state transitions in public domain single-cell RNA-sequencing (scRNA-seq) data of 25,422 epithelial cells from pancreatic ductal adenocarcinoma (PDAC) tumors and control samples. <strong>The first</strong> demonstrates <strong><a href="https://github.com/FertigLab/pycogaps" target="_blank">PyCoGAPS</a></strong>, our new Python implementation of CoGAPS that enhances runtime of Bayesian NMF for large datasets.</p>

<img src="images/figure1.png" align="right" style="margin: 0px 10px 80px 20px;" />
<p><strong>The second</strong> procedure steps through the same single-cell NMF analysis using our <strong><a href="https://github.com/FertigLab/CoGAPS" target="_blank">R CoGAPS interface</a></strong>, and <strong>the third</strong> introduces a beginner-friendly CoGAPS platform using GenePattern Notebook. By providing Python support, cloud-based computing options, and relevant example workflows, we facilitate user-friendly interpretation and implementation of NMF for single-cell analyses. The expected timing to properly setup the packages and conduct a test run is around 15 minutes, and an additional 30 minutes to conduct analyses on a precomputed result. The expected runtime on the user’s desired dataset can vary from hours to days depending on factors such as the size of the dataset or input parameters.</p>

|                                    |                                                       |                         **Workflow Comparison**                        |                                      |                                                                                        |
|:----------------------------------:|:-----------------------------------------------------:|:----------------------------------------------------------------------:|:------------------------------------:|:--------------------------------------------------------------------------------------:|
|        **Procedure Choice**        |               [**Procedure 1:  PyCoGAPS**](/CoGAPSGuide/procedureone)              |                                                                        |       [**Procedure 2:  CoGAPS**](/CoGAPSGuide/proceduretwo)      |                         [**Procedure 3:  GenePattern Notebook**](/CoGAPSGuide/procedurethree)                         |
|            Option Choice           |               [Option A:  Python scripts](/CoGAPSGuide/optiona)               |                            [Option B:  Docker](/CoGAPSGuide/optionb)                           |                  --                  |                                           --                                           |
|              Overview              | Write and call functions in any Python supported IDE. | Easily plug in parameters and run code in a prepared Docker container. | Write and call functions in RStudio. | Easily plug in parameters and run pre-written code cells in a web browser environment. |
|   Preferred programming language   | Python                                                | Python / no preference                                                 | R                                    | Python / no preference                                                                 |
| Recommended programming experience | Experienced                                           | Little to none                                                         | Experienced                          | Little to none                                                                         |
|        Install dependencies?       | Yes                                                   | No                                                                     | Yes                                  | No                                                                                     |
|      Customization flexibility     | High                                                  | Limited                                                                | High                                 | Limited                                                                                |
|         Parameter handling         | Call functions                                        | Easy plug-in                                                           | Call functions                       | Easy plug-in                                                                           |
|            Run location            | Locally or own server                                 | Locally or own server                                                  | Locally or own server                | Remotely on AWS server                                                                 |
