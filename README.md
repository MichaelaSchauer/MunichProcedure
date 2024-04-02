__The Munich Procedure__

The provided R-Script **decribes the Munich Procedure** designed by Michaela Schauer (**Schauer 2024**) which is **based on the Frankfurt Procedure** developed by Dr Markus Helfert and **takes this approach a step further**: The Frankfurt Procedure compares values measured by p-XRF (x-values or independent variable) with values of the same set of samples obtained by a laboratory method - in this case WD-RFA (y-values or dependent variable). A coefficient correction (coefcor) is applied by using the calculated slope and, if appropriate, intercept to correct the p-XRF values to match those of the laboratory method. In addition, the same approach can be used to compare data obtained from the same instrument before and after a change of set-up by the manufacturer. The Munich Procedure additionally provides the calculations as R-scripts and adds quality criteria such as rSEE, RMS and CI, as well as the associated graphical output.

The Script **MunichProcedure.qmd** provides an example for the application of the Munich Procedure explaining all necessary calculations and decisions in detail. It guides through the development of a coefcor for the element **aluminium** by **comparing p-XRF and WD-RFA values** from measurements of the **Frankfurt pottery sample set**. The p-XRF data used are from the first data set taken by the Niton XL3t No 97390 of the Department for Cultural Sciences of the Ludwig-Maximilians-University Munich - namely coefcor I (see Schauer 2023/2024). 

The code was written using RGUI version 4.3.1, RCMDR version 2.8-0 and RStudio version 2023.06.1 with Quarto version 1.3.433. It is executable, i.e. it is fully functional.

The sources used to create the code for each chapter can be found under 'source' and are only presented when the code is first introduced.

__Literature:__ 

Schauer, Michaela 2024: Coefficient corrections for portable X-ray fluorescence data of the Niton XL3t No. 97390 (coefcor I-IV) developed according to the Munich procedure. Data in Brief 53. 109914. https://doi.org/10.1016/j.dib.2023.109914

Schauer, Michaela 2023: R-scripts and data of coefficient corrections developed since 2017 for the Niton XL3t No. 97390 following the Munich Procedure. 12. September 2023. Open Data LMU. https://doi.org/10.5282/ubm/data.405
