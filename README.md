# Data Wrangling Project Template

## About this template

The organizational structure (i.e., the specific way in which the files are nested within folders) of this repository is based on Project TIER's Documentation Protocol (version 4.0). [Project TIER](https://www.projecttier.org) (Teaching Integrity in Empirical Research), based out of Haverford College, is a multidisciplinary initiative created to promote reproducible data workflows in undergraduate curricula. In addition to hosting pedagogical training workshops for educators, Project TIER also maintains a guide, called the [TIER Protocol](https://www.projecttier.org/tier-protocol/protocol-4-0/), that outlines best practices in reproducible analysis. While this repository template takes considerable inspiration from the TIER Protocol, it differs in a couple key ways:

1.  It simplifies the TIER Protocol in a way that is commensurate with the scope of the class project it is associated with.

2.  It forgoes the nomenclature introduced by TIER Protocol 4.0 in favor of file names that more consistently align with the terminology introduced in our textbook, [R for Data Science (2e)](https://r4ds.hadley.nz).

## Template organization and function

The following directory tree (based on TIER Protocol 4.0) provides a simple visualization of the template's organizational structure.

-   project/

    -   README.md

    -   final_data.csv

    -   example_analysis.qmd

    -   data/

        -   imported_data/

            -   metadata/

                -   source.txt

                -   codebook.txt

        -   cleaned_data/

            -   metadata/

                -   source.txt

                -   codebook.txt

    -   scripts/

        -   import.qmd

        -   cleaning.qmd

        -   exploration.qmd

    -   output/

### README.md

Well would you look at that, you're reading through the README.md file right now! I bet you can even intuit a bit of the purpose of this document based on what you've read so far. In short, the README.md file is the "user manual" for your project. Because it functions to summarize the project, the README.md is the last document written. It is composed of three sections:

1.  Software and platform

    -   Software (R, RStudio, Git) and packages (e.g., httr2, rvest, tidyr, etc.) including version numbers

    -   Platform (Windows, macOS) including version numbers

2.  Documentation map

    -   A map of your directory tree (see the example above) that includes all files and folder in your project

3.  Instructions for reproducing your work

    -   Step-by-step instructions that make it possible for a person unfamiliar with your project to reproduce the final_data.csv file

    -   These instructions should walk through the documentation map, clearly outlining the relationships between scripts and files (e.g., the data/imported_data/example.csv file is passed into scripts/cleaning.qmd to produce final_data.csv)

### final_data.csv

Major project products are given at the top-level (i.e., not nested within sub-folders) of the repository. In most cases, the major product will be some sort of report that incorporates exploration, visualization and modeling to address a problem or answer a question. In the context of this project, the major product is the dataset you've successfully wrangled from the web.

### example_analysis.qmd

The example analysis notebook that accompanies and illustrates the utility of final_data.csv is also a product of this project (albeit a less important one), and so also lives at the top level of the repository.

### data/

The data/ folder contains two sub-folders: (1) imported_data/ and (2) cleaned_data/. The imported_data/ folder will contain the data (as uncleaned R object files) you've gathered through API queries and web scraping. The cleaned_data/ folder will contain the dataset(s) that has/have been processed by the scripts/cleaning.qmd file.

### scripts/

The scripts/ folder contains three Quarto notebooks: (1) import.qmd, (2) cleaning.qmd, and (3) exploration.qmd. All code related to the import of data (i.e., your `{httr2}` and `{rvest}` code) should be [well-annotated]{.underline} and organized within import.qmd. All cleaning activities (e.g., rectangling, reshaping, parsing, coercion, recoding, etc.) should be [well-annotated]{.underline} and organized within cleaning.qmd. Finally, a thoughtful exploration of the data should appear in exploration.qmd (again, [well-annotated]{.underline} and organized).

### output/
