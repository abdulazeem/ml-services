# Managed Services for Machine Learning
This repository is a summary of the content of lesson six of the *Introduction to Machine Learning on Azure* course which is part of the *Microsoft Scholarship Foundation course Nanodegree Program* on *Udacity* (July - September 2020).

As part of our role as student leaders, we will not only write this guide book, but also answer commonly asked question of the community. Furthermore, we will provide a list of resources to support your success in this course.

**You can do it!**

## Introduction

Managed services for Machine Learning can be used to *outsource* your local Machine Learning processes (Training, Inference and Notebook Testing) to the cloud. By using end-to-end automation via pipelines (DevOps for ML / MLOps), you can deploy to production environments easily. The examples in this lesson will use services provided by Azure Machine Learning.

In comparison to local development, you don't need to install any applications and libraries, as all this has been done already. You don't have to take care of the *low level* layers, so you can jump right in using your webbrowser!

Speaking of using your webbrowser, you might already know from the previous lessions, that you need to prelaunch your lab environment to get the scholarship account details. Visit [this page](https://classroom.udacity.com/nanodegrees/nd00332/parts/9e5002de-e740-4eb2-aa15-03861fff12fc/modules/ae74a72a-97c1-4306-b55e-708c58118bd2/lessons/ff14cb2c-d367-4f57-9f35-244fd1aceda2/concepts/0d9d532d-d0e3-4a76-bfa3-fd6630372628) and click on the blue *Prelaunch Lab* button before moving on.


## Labs
### Lab 1: Managing Compute Resources
In this lab, you will learn how to create a new compute resource, how to modify an existing one and how to stop, restart or delete it.

1. [Open Workspace](https://classroom.udacity.com/nanodegrees/nd00332/parts/9e5002de-e740-4eb2-aa15-03861fff12fc/modules/ae74a72a-97c1-4306-b55e-708c58118bd2/lessons/ff14cb2c-d367-4f57-9f35-244fd1aceda2/concepts/50fa8755-d4eb-413d-9b5d-6277671452b2)
2. Enter the *Studio* by clicking *Launch now* and select a subscription and workspace as mentioned in the lab guide.
3. Select *Compute* in the right menu.
4. Select the *Compute instances* tab.
5. Click on the *Create* button, choose a unique name of your choice and select a virtual machine from the dropdowns. For this lession, we will be using a CPU-based VM with size *Standard_D3_v2*.
6. Click on *Create* and wait a few seconds (took 8 minutes in my case) until the shown status changes to *Running*.
7. Select your compute resource in the list and click on its name to view details about the compute. You can also click on any of the buttons to stop, delete or restart the resource.
8. Go back to the list of computes and take a look at the *Application URI* column. By clicking on any of the links, a new browser tab with the respective development environment will be launched. 
![screenshot of the list of compute resources](images/lab-1-list.jpg)

### Lab 2: Managed Notebook Environments
In this lab, you will learn how to train a simple SciKit learn model using a managed notebook environment.

1. [Open Workspace](https://classroom.udacity.com/nanodegrees/nd00332/parts/9e5002de-e740-4eb2-aa15-03861fff12fc/modules/ae74a72a-97c1-4306-b55e-708c58118bd2/lessons/ff14cb2c-d367-4f57-9f35-244fd1aceda2/concepts/d3b43f98-bd8b-4c5d-ba6d-c19cbdd5bfd0)
2. Open the *Studio* and navigate to the *Compute* tab, just as you did in the last lab. Note that you won't need to create a new instance this time, as the workspace will already have one prepared for you.
3. In the *Application URI* column, click on the *Jupyter* link.
4. In Jupyter, open a terminal by clicking on *New* and *Terminal*
5. Download an example notebook by using `git clone https://github.com/solliancenet/udacity-intro-to-ml-labs.git`
6. From within the Jupyter interface, navigate to directory `udacity-intro-to-ml-labs/aml-visual-interface/lab-19/notebook` and open `1st-experiment-sdk-train-model.ipynb`.
7. Read through the notebook to get a quick overview
8. Select "Cell" and "Run All" ´, click on the login-link in the first cells output and then wait for the run to be completed.
9. in the directory `udacity-intro-to-ml-labs/aml-visual-interface/lab-19/notebook/outputs`, you will find the trained `.pkl` model file for each iteration.
![screenshot of the generated output](images/lab-2-output.jpg)
10. *Optional:* Modify the notebook as you want and re-run code by clicking on "Kernel" and "Restart & Run All". 


## About

### Contributing
Feel free to send pull requests or open an issue if you have any questions.

 All commit messages should follow the [Udacity Git Commit Message Style Guide](https://udacity.github.io/git-styleguide/).

### License
The content of this repository is released under the [MIT license](LICENSE).