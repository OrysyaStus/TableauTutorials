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
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/TabPy.PNG">
This dashboard utilizes a deployed function from a Jupyter notebook. Changes to the user-inputted parameters allow for real-time predictions. The data used for this work is taken from the UC Irvine machine learning repository: https://archive.ics.uci.edu/ml/datasets/Heart+Disease

## 1. TabPy Server Set Up
Go to https://github.com/tableau/TabPy to download/clone TabPy as needed:
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/TabPy_Setup_1.PNG">

Full instructions: https://github.com/tableau/TabPy/blob/master/server.md
1. No Python or Anaconda installation: https://github.com/tableau/TabPy/blob/master/server.md#using-the-setup-script
2. Have Anaconda for Python 2.7: https://github.com/tableau/TabPy/blob/master/server.md#manual-installation

**Must: pip install tabpy-server**

## 2. TabPy Client Set Up
Full instructions: https://github.com/tableau/TabPy/blob/master/client.md
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/tabpy_client.PNG">

**Must: pip install tabpy-client**

## 3. Install Tableau 10.3
If needed: https://github.com/OrysyaStus/TableauTutorials

## 4. Start Tableau Server
Open a command prompt. Navigate to the tabpy_server folder under site-packages and run startup.bat or startup.sh on Windows and Linux/MacOS respectively. 

Example path for Windows (note this will be different for each computer)
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/start_tableau_server.PNG">
Make sure to keep this command prompt running in the background until the end of the tutorial.

## 5. Create External Service Connection in Tableau
Open SanDiegoMapping.twbx into Tableau Desktop. 

Choose 'Yes' to run external service scripts. <br>
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/run_external_service.PNG">

If additional errors pop up, ignore them as we will fix these.

Make sure that external service connection in Tableau is made.<br>
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/external_service_connection1.PNG">
<br><br>Choose correct server and port.<br>
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/external_service_connection2.PNG">
<br>'Test Connection' to make sure that a connection with Tableau Server has been made.

## 6. Understanding Difference between Inline and Deployable Functions
1. Python inline scripting as a Tableau calculated field
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/inline_example.PNG">
Link: https://www.tableau.com/about/blog/2017/1/building-advanced-analytics-applications-tabpy-64916

2. Python deployable function from Jupyter notebook
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/deployable_function.PNG">
Link: https://www.tableau.com/about/blog/2017/1/building-advanced-analytics-applications-tabpy-64916

We will be focusing on the deployable functions for this tutorial.

## 7. Process, Model, and Predict with Jupyter Notebook
Open a new command prompt, navigate to location of HD_ML_Example.ipynb and start a Jupyter Notebook.
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/start_jupyter_notebook.PNG">

Work through the Jupyter notebook
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/jupyter_notebook.PNG">

## 8. Deploy Function into Tableau
After selecting the desired model, deploy your function into Tableau.
<img src="https://github.com/OrysyaStus/TableauTutorials/blob/master/TabPy_Python_Integration/Images/deploy_function.PNG">



