# CrawlingBandit_public

Original repository is private. Please contact me if you want access to the project. 

You will find below the Readme file from the project.


# Crawling Bandits: Exploring a stochastic graph with limited visibility using bandits

This repository presents Abderrahim and I's work on stochastic graph exploration. 
This work was done as a part of our class on Graphs in Machine Learning (http://researchers.lille.inria.fr/~valko/hp/mva-ml-graphs.php) by Michal Valko.
In this project, we study the crawling stochastic bandits problem under local visibility constraints. 
We first implemented the NetExp [1] algorithm for graph exploration, then we implement a solution to the stochastic version of the problem based on UCB and proposed by a previous team. Finally we derived our own version of another stochastic algorithm an compared the results.

Our goal was to find an effective way to gather information in a network where each node’s visibility is limited to its local neighbourhood. 
Our main contribution was the use of a modified version of Thompson Sampling to tackle the exploration/exploitation dilemma.
We obtained better results (using cumulated regret as a metric) than other algorithms.

[1] Adish Singla et al, Information Gathering in Networks via Active Exploration, 2015, https://las.inf.ethz.ch/files/singla15netexp.pdf

## Data

We used synthetic datasets formed with NetworkX.

We also used two datasets from Stanford (https://snap.stanford.edu/): the YouTube and Facebook one.

## Getting Started

You can just run the notebook once you have installed the different python modules (see below for a list of modules to install).

Description of the files
* util_functions.py > Gathers functions that we use many times in algorithms.py.
* algorithms.py > Gathers our implementation of the algorithms that we coded using previous papers (NetExp, , Stochastic-NetExp, GraBaVic) and the algorithm that we derived ourselve (GraBaVic-TS).
* simple_graph.ipynb > Tests of our algorithm on a simple graph and comparison with the existing methods.
* parameter_optimization.ipynb > Optimization of the parameter gamma on the simple graph.
* Youtube.ipynb > Test of our algorithm on the YouTube dataset from Stanford datasets and comparison with the existing methods.
* facebook.ipynb > Test of our algorithm on the facebook dataset from Stanford datasets and comparison with the existing methods.

### Prerequisites

You should install the following modules, for instance through pip:

```
pip install --upgrade numpy matplotlib seaborn networkx scipy joblib pathos
```

## Built With

* Python 3
* Jupyter Notebook

## Authors

* **Abderrahim Ait Azzi**
* **Maxime Wabartha**


## Acknowledgments

* Previous team that derived the GraBaViC algorithm.

