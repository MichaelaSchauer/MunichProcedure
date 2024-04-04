## The Munich Procedure

The provided R-Script **decribes the Munich Procedure** designed by Michaela Schauer (**[Schauer 2024](https://doi.org/10.1016/j.dib.2023.109914)**) which is **based on the Frankfurt Procedure** developed by Dr Markus Helfert but **takes this approach a step further**: The Frankfurt Procedure compares values measured by p-XRF (x-values or independent variable) with values of the same set of samples obtained by a laboratory method - in this case WD-RFA (y-values or dependent variable). A coefficient correction (coefcor) is applied by using the calculated slope and, if appropriate, intercept to correct the p-XRF values to match those of the laboratory method. In addition, the same approach can be used to compare data obtained from the same instrument before and after a change of set-up by the manufacturer. The Munich Procedure additionally provides the calculations as R-scripts and adds quality criteria such as rSEE, RMS and CI, as well as the associated graphical output.

The Script **MunichProcedure.qmd** provides an example for the application of the Munich Procedure explaining all necessary calculations and decisions in detail. It guides through the development of a coefcor for the element **aluminium** by **comparing p-XRF and WD-RFA values** from measurements of the **Frankfurt pottery sample set**. The p-XRF data used are from the first data set taken by the Niton XL3t No 97390 of the Department for Cultural Sciences of the Ludwig-Maximilians-University Munich - namely coefcor I (see [Schauer 2023](https://doi.org/10.5282/ubm/data.405)/[2024](https://doi.org/10.1016/j.dib.2023.109914)). 

Since the data has been structured in the form of an **R project**, the entire MunichProcedure folder can be **downloaded and run locally**.

The code was written using RGUI version 4.3.1, RCMDR version 2.8-0 and RStudio version 2023.06.1 with Quarto version 1.3.433. It is executable, i.e. it is fully functional. The necessary R-Packages are specified in the code-file. As .qmd-files use other ways to mark text and r-code then .r or .rmd-files, the folder Munich Procedure also includes a **.html and .pdf-file of the original code**.

The sources used to create the code for each chapter can be found under 'source' and are only presented when the code is first introduced.

### Literature

[Schauer, Michaela 2024](https://doi.org/10.1016/j.dib.2023.109914): Coefficient corrections for portable X-ray fluorescence data of the Niton XL3t No. 97390 (coefcor I-IV) developed according to the Munich procedure. Data in Brief 53. 109914. 

[Schauer, Michaela 2023](https://doi.org/10.5282/ubm/data.405): R-scripts and data of coefficient corrections developed since 2017 for the Niton XL3t No. 97390 following the Munich Procedure. 12. September 2023. Open Data LMU. 

## Additional guidance

In order to be able to work with the R script provided, the most important practical steps required to get started are briefly explained below. However, this is no substitute for studying the programme itself and the contents of the scripts. [Siegmund 2020](https://www.frank-siegmund.de/veroeffentlichungen/i-monographien/lehrbucharchaeostatistik) is recommended as a basis in German, as an introduction to the R plugin Quarto [his guide](https://www.frank-siegmund.de/images/opendata/EinfuehrungQuarto.zip) from 2023. In English, the [RQuarto website](https://quarto.org/) is most useful. [Field et al. 2013](https://archive.org/details/discoveringstatisticsusingr/page/n9/mode/2up) is also worth reading, entertaining and contains all the relevant information for getting started. The operators of R provide a regularly updated introduction; the current version can be found [here](https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf).  

### R, RStudio and RQuarto

RConsole is the 'raw' R, i.e. it works entirely with code. RStudio, on the other hand, has a user interface that accesses RConsole. For the R script presented here, RStudio was used in conjunction with Quarto, an R-specific writing environment that greatly simplifies the handling of code during both development and publication. Quarto allows individual R scripts to be created in the form of Quarto files (.qmd) and exported in various other formats (.html, .pdf). In addition to the 'pure' R code, further information about the code modules can also be provided. To work with this script, it is recommended to install [RConsole as well as RStudio](https://www.rstudio.com/products/rstudio/download/) and [Quarto](https://quarto.org/docs/download/).

Quarto documents contain 'executable' R code, i.e. they have been developed and extensively tested to perform the desired calculations without error. When the Quarto files are opened in RStudio, the code blocks are highlighted in grey. They can be executed by clicking on the small green arrow at the top right of the code block. If only one or a few lines of code are to be executed, they can be selected and executed using Ctrl+Enter. More information about Quarto and Quarto code can be found [here](https://quarto.org/).

### RProjects

To ensure that the calculations run smoothly, the script has been embedded in an R project. The Rproject file (.Rproj) is located in the parent folder of the calculations and can be opened by double-clicking. The file path is defined in this file, so as long as the data is in the same folder, the whole project can be saved anywhere and the code will work. The only requirement is that the code snippet stored in the working directory setting file is loaded the first time it is used. Another advantage of RProjects is that all Quarto files opened during project creation are loaded directly when the project is opened - there is no need to search the file structure. 

### R Packages
Packages must be installed to run the calculations. The packages only need to be installed the first time they are used, after that they need to be reloaded for each session. These packages contain functions that are required to calculate certain analyses. They need to be installed and loaded. The packages can be installed in RStudio by clicking on Packages - Install package(s) - selecting the geographically closest CRAN Mirrow, then locating the package, clicking on it and clicking OK. Another option is to use R code with the package name in parentheses:

install.packages("ggplot2")

The packages will be loaded with the code

library(ggplot2)

A brief introduction to the basic codes can also be found, for example, [here](https://cran.r-project.org/doc/contrib/Paradis-rdebuts_en.pdf ).
