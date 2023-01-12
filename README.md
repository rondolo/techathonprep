# techaton-knowledge-graphs

This repository contains code, explanations and assignments related to Knowledge Graphs techathons.

Preparations

1. Make sure you've cloned this repository and that you have Docker/Podman ready on your machine. Also make sure to pull the Docker image listed below. During the assignments you'll create your own results folder from a template. Make sure to commit and push your results folder at the end of the techaton.

    Clone this repository
        git clone https://github.com/DataScienceOrdina/techaton-knowledge-graphs
    Pull Docker image
        docker pull docker.io/jupyter/datascience-notebook:2022-07-11


Next, we will need to get the jupyter/datascience-notebook up and running. If you don't already have it, you can pull the image by running 

    podman pull docker.io/jupyter/datascience-notebook
    or
    docker pull docker.io/jupyter/datascience-notebook

Now we start the notebook server by running: On MacOS/Linux

    podman run -it --rm -p 8888:8888 -v "${PWD}":/home/jovyan/work jupyter/datascience-notebook
    or
    docker run -it --rm -p 8888:8888 -v "${PWD}":/home/jovyan/work jupyter/datascience-notebook:2022-07-11

On Windows

    podman run -it --rm -p 8888:8888 -v ".":/home/jovyan/work jupyter/datascience-notebook
    or
    docker run -it --rm -p 8888:8888 -v ".":/home/jovyan/work jupyter/datascience-notebook:2022-07-11

Now follow the link in your terminal to open the Jupyterlab environment. Unfortunately, spaCy, neo4j and wikipedia are not installed by default on the datascience image, so we will have to install it. This can be done by opening a terminal inside the jupyterlab environment and executing:

pip install spacy
pip install spacy-transformers
pip install wikipedia
pip install neo4j 
python -m spacy download en_core_web_sm
python -m spacy download en_core_web_md

Copy the the notebook Techathon Knowledge Graphs 12 January 2023 and give it your (team)name. Make sure you store all your progress in this folder during this assignment.

