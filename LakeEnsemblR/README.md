# Ensemble lake modelling with LakeEnsemblR
<a href="url"><img src="logo.png" align="right" height="220" width="220" ></a>

-----

:spiral_calendar: October 15, 2020  
:alarm_clock:     15:00-17:00 CEST 
:busts_in_silhouette: Jorrit Mesman, Johannes Feldbauer, Tadhg Moore, Robert Ladwig   
:computer: [Material](https://github.com/gsagleon/G21.5_GSA_workshop/tree/master/LakeEnsemblR)  
:octocat: [Homepage](https://github.com/aemon-j/LakeEnsemblR)

-----

## Description

A guided walkthrough of the new [R package “LakeEnsemblR”](https://github.com/aemon-j/LakeEnsemblR) that has been developed within the GLEON modelling group. Learn how to set up multiple lake models for your lake physical system, how to calibrate your models and explore model uncertainty. Brainstorming of further ideas for how this package can be applied to aid further research. Everyone is welcome to attend, but the workshop is mostly aimed at people with at least some experience in lake modelling. 

## What will this workshop cover?

Introduction to LakeEnsemblR package:
  - Why use ensembles?
  - What is LakeEnsemblR?

Using LakeEnsemblR:
  - Standardisation of input data
  - Functions
  - Visualising output & calibration
  - Apply it to YOUR lake! (or on OUR examples)

Future plans regarding LakeEnsemblR:
  - Adding more models
  - Creating a static WQ model
  - Potential applications
  - Stick around to talk about questions and raise issues 

## Prerequisites

There are two paths to follow the workshop examples:
  ### 1. Use Github and your local R setup
  Clone or download files from this Github repository. 
  You’ll need R (version >= 3.5), preferably a GUI of your choice (e.g., Rstudio) and these packages: 
  ``` 
  require("devtools")
  devtools::install_github("GLEON/rLakeAnalyzer")
  devtools::install_github("USGS-R/glmtools", ref = "ggplot_overhaul")
  devtools::install_github("GLEON/GLM3r", ref = "GLMv.3.1.0a3")
  devtools::install_github("aemon-j/FLakeR", ref = "inflow")
  devtools::install_github("aemon-j/GOTMr")
  devtools::install_github("aemon-j/gotmtools")
  devtools::install_github("aemon-j/SimstratR")
  devtools::install_github("aemon-j/MyLakeR")
  devtools::install_github("aemon-j/LakeEnsemblR")
  ```
  ### 2. Use Docker
  To be sure that all the examples will *work* during the workshop, you can use a [container](https://hub.docker.com/r/hydrobert/lakeensemblr-rocker) of all the material. I'll quote the Docker website here: 
  > "A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings." 
  
  You can install the Docker software from [here](https://docs.docker.com/get-docker/). Once installed, you'll need to open a terminal and type (the pulling will take some time depending on your internet connection, it's about 4 Gb big)
  ```
  docker pull hydrobert/lakeensemblr-rocker
  docker run --rm -d  -p 8000:8000 -e ROOT=TRUE -e PASSWORD=password hydrobert/lakeensemblr-rocker:latest
  ```
  Then, open any web browser and type ‘localhost:8000’ and input user: rstudio, and password: password. Rstudio will open up with the script and data available in the file window. 

## Files
  
  The HTML and PDF files in the repository both contain the information needed for the workshop. You can pick which one you prefer. You can copy the code into an R script and run it yourself, or use the pre-made R script ("G21_5_Workshop_LakeEnsemblR.R"), which contains all the lines of code that are run during the workshop and some short comments. 

-----

