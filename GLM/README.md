# Process-based lake modeling in R using GLM (General Lake Model)
<a href="url"><img src="GLM_hex.png" align="right" height="220" width="220" ></a>

-----

:spiral_calendar: October 14, 2020  
:alarm_clock:     14:30 - 17:00 GMT (09:30 - 12:00 CDT)  
:busts_in_silhouette: Robert Ladwig, Aryan Adhlakha, Hilary Dugan & Paul Hanson    
:computer: [Material](https://github.com/robertladwig/GLM_workshop) 
:open_book: [Presentation](https://github.com/gsagleon/G21.5_GSA_workshop/blob/master/GLM/GLM_workshop.pdf)

-----

## Description

The aim of this workshop is (1) to give a general introduction to process-based modeling and GLM-AED2; (2) highlight the application of GLM-AED2 in R (glmtools, GLM3r, LakeEnsemblR); and (3) applying the model to a real-world case, e.g. model calibration, output post-processing and interpreting water quality results. This workshop is intended for all skill levels, although prior knowledge of R is helpful. If you just want to watch, ask questions, and drive from the back seat, that’s fine, too!

## What will this workshop cover?

Introduction to process-based lake modeling (get the slides [here](https://github.com/gsagleon/G21.5_GSA_workshop/blob/master/GLM/GLM_workshop.pdf)):
  - What is process-based modeling?
  - GLM theory and applications
  - AED2 theory and examples for oxygen and carbon
  - Overview of available R-packages
  
Using the model in R:
  - Running GLM in R
  - Visualising results
  - Calibrating water temp. and oxygen parameters
  - Checking your phytoplankton

Questions and problems:
  - Stick around to talk about questions and raise issues 
  
## Questions or issues?
Feel free to write me an email at rladwig2@wisc.edu, and/or join the [official GLM slack channel](https://join.slack.com/t/general-lake-model/shared_invite/zt-a7pyrxhj-oe4dYm6oLQfk1r_ZGLFTwQ).
During the workshop you can ask urgent questions directly any time by 'raising your hand' in Zoom. 
Otherwise, you can also post your questions in [this google doc](https://docs.google.com/document/d/1uKsswTH4W1qZe8smbGfnsfKMdcur_cPIHcCMpI3GsPM/edit?usp=sharing) and we will talk about it at the end of the workshop. Or, if there's no time left, I can email you the answer if you provide your email address in the google document. There's also time to ask questions at the end of the workshop.

## Prerequisites
  
  ### Word of caution
This workshop example was tested on General Lake Model (GLM) Version 3.1.0b1. The setup may not work using older and more recent versions of GLM.

There are two paths to follow the workshop examples:
  ### 1. Use Github and your local R setup
  Clone or download files from this [Github repository](https://github.com/robertladwig/GLM_workshop). 
  You’ll need R (version >= 3.5), preferably a GUI of your choice (e.g., Rstudio) and these packages: 
  ``` 
  require(devtools)
  devtools::install_github("GLEON/GLM3r", ref = "GLMv.3.1.0a3")
  devtools::install_github("hdugan/glmtools", ref = "ggplot_overhaul")
  install.packages("rLakeAnalyzer")
  install.packages("tidyverse")
  ```
  ### 2. Use Docker
  To be sure that all the examples will *work* during the workshop, you can use a [container](https://hub.docker.com/r/hydrobert/glm-workshop) of all the material. I'll quote the Docker website here: 
  > "A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings." 
  
  You can install the Docker software from [here](https://docs.docker.com/get-docker/). Once installed, you'll need to open a terminal and type (the pulling will take some time depending on your internet connection, it's 3.87 Gb big)
  ```
  docker pull hydrobert/glm-workshop
  docker run --rm -d  -p 8000:8000 -e ROOT=TRUE -e PASSWORD=password hydrobert/glm-workshop:latest
  ```
  Then, open any web browser and type ‘localhost:8000’ and input user: rstudio, and password: password. Rstudio will open up with the script and data available in the file window. 
  
  After you have finished the workshop examples, you can close the docker application by running
  ```
  docker kill $(docker ps -q)
  docker rm $(docker ps -a -q)
  ```
  
  
-----
