# TabPy: Python Integration with Tableau
This tutorial will introduce TabPy, an API which makes it possible to use Python scripts (either inline or deployed function) as a Tableau calculated field. This is an advanced feature in Tableau which allows combining trained machine learning models in Python with Tableau visualizations. 

Additional resources about TabPy:
1. https://www.tableau.com/about/blog/2017/1/building-advanced-analytics-applications-tabpy-64916
2. https://www.tableau.com/about/blog/2016/11/leverage-power-python-tableau-tabpy-62077
3. https://github.com/tableau/TabPy

TabPy drawbacks:
1. Currently in beta
2. For entire deployable functionality, need to have access to Tableau Server

This tutorial will be using the following work https://sandiegohearts.github.io/

We will understand the setup and functionality of TabPy using a working example
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/Python_Integration/Images/TabPy.PNG">
This dashboard utilizes a deployed function from a Jupyter notebook. Changes to the user-inputted parameters allow for real-time predictions. The data used for this work is taken from the UC Irvine machine learning repository: https://archive.ics.uci.edu/ml/datasets/Heart+Disease

## Set Up
1. Install Python (Anaconda)
    Windows: https://medium.com/@GalarnykMichael/install-python-on-windows-anaconda-c63c7c3d1444
    Mac: https://medium.com/@GalarnykMichael/install-python-on-mac-anaconda-ccd9f2014072
    Linux: https://medium.com/@GalarnykMichael/install-python-on-ubuntu-anaconda-65623042cb5a
2. 
