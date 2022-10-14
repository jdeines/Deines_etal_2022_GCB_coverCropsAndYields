# Deines, Guan, Lopez, Zhou, White, Wang, and Lobell 2022, Global Change Biology
## Derived data and analysis code

14 October 2022  
Code by: Jillian Deines, with contributions from Cambria White and Bruno Lopez  
Contact: jillian.deines@gmail.com  

This codebase accompanies the paper:

Deines, JM, K. Guan, B. Lopez, Q. Zhou, C. White, S. Wang, and D.B. Lobell. 2022. Recent cover crop adoption is associated with small maize and yield losses in the United States. Global Change Biology, https://doi.org/.....

## Contents and Subfolders

### Manuscript
The preprint version of the manuscript (post-revisions, pre-formatting) and supplement 

### Data
All data needed to reproduce the figures presented in the manuscript can be found in the `data` folder. Raw input data are available at their respective sources as described in the manuscript.

**Data included**

* `data/cleanedPointSample`: The full point samples used in analysis are in this folder, along with causal forest output used to make Figures 5-8. This includes (1) the point sample dataset underlying the analysis for a) maize, b) soybeans, and c) the maize placebo test. We have removed the latitude and longitude coordinates from this dataset for data privacy concerns, so points can only be located to the county level. (2) variable importance output from the causal forests, used in Figs 6 and 8. (3) causal forest output (conditional average treatment effects, or CATEs) needed for Figures 5 - 8; again, the location information has been removed beyond the county level.
* `data/stateTrends_RS_nass`: Summary data on cover crop acreage by county from (1) USDA NASS statistics and (2) summarized remote sensing datasets. This data is used in Figures 1 and 2
* `data/gis`: GIS files used in figure creation, including (1) state boundaries, and (2) countie boundaries, and (3) raster geotiffs of the CATE yield effects from Figures 5 (maize) and 7 (soybeans)


### Code
* Code to perform all paper analyses and generate figures in the paper 

Script filenames are numbered in sequential order of use. Processing is done using [R Markdown](https://rmarkdown.rstudio.com/) within an R project structure. Operational scripts have extension .Rmd; notebook style docs (code + outputs) available in two formats (a .md for easing viewing on Github and .html for desktop viewing) are also provided.

Note that the causal forest analysis as written in scripts 02.06 - 02.22 will not run, since the latitude and longitude have been removed from the data. Running the analysis without these variables will not give identical results to that presented in the paper. All analysis output used to make the figures, however, is provided.

### Figure
Figure output from scripts used to generate figures in the main text.

