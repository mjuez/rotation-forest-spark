# Rotation Forest for Big Data

[https://doi.org/10.1016/j.inffus.2021.03.007](https://doi.org/10.1016/j.inffus.2021.03.007)

Mario Juez-Gil <<mariojg@ubu.es>>, Álvar Arnaiz-González, Juan J. Rodríguez, Carlos López-Nozal, and César Ignacio García-Osorio.

**Affiliation:**\
Departamento de Ingeniería Informática\
Universidad de Burgos\
[ADMIRABLE Research Group](http://admirable-ubu.es/)\
Burgos\
Spain

## Abstract

The Rotation Forest classifier is a successful ensemble method for a wide variety of data mining applications. However, the way in which Rotation Forest transforms the feature space through PCA, although powerful, penalizes training and prediction times, making it unfeasible for Big Data. In this paper, a MapReduce Rotation Forest and its implementation under the Spark framework are presented. The proposed MapReduce Rotation Forest behaves in the same way as the standard Rotation Forest, training the base classifiers on a rotated space, but using a functional implementation of the rotation that enables its execution in Big Data frameworks. Experimental results are obtained using different cloud-based cluster configurations. 
Bayesian tests are used to validate the method against two ensembles for Big Data: Random Forest and PCARDE classifiers. Our proposal incorporates the parallelization of both the PCA calculation and the tree training, providing a scalable solution that retains the performance of the original Rotation Forest and achieves a competitive execution time (in average, at training, more than 3 times faster than other PCA-based alternatives). In addition, extensive experimentation shows that by setting some parameters of the classifier (i.e., bootstrap sample size, number of trees, and number of rotations), the execution time is reduced with no significant loss of performance using a small ensemble.

## Experiments

The experiments are available in [this notebook](experiments.ipynb).

## Implementation

The implementation is available in [this repository](https://github.com/mjuez/rotation-forest-bd).

## Aknowledgements

This work was supported through project TIN2015-67534-P (MINECO/FEDER, UE) of the *Ministerio de Economía y Competitividad* of the Spanish Government, projects BU085P17 and BU055P20 (JCyL/FEDER, UE) of the *Junta de Castilla y León* (both projects co-financed through European Union FEDER funds), and by the *Consejería de Educación* of the *Junta de Castilla y León* and the European Social Fund through a pre-doctoral grant (EDU/1100/2017). The project leading to these results has received also funding from "la Caixa" Foundation, under agreement LCF/PR/PR18/51130007. This material is based upon work supported by Google Cloud.

## Citation policy

Please cite this research as:

```
@ARTICLE{juezgil2021rotfbd,
title = {Rotation Forest for Big Data},
author = {Juez-Gil, Mario and Arnaiz-Gonz{\'a}lez, {\'A}lvar and Rodr{\'\i}guez, Juan J and L{\'o}pez-Nozal, Carlos and Garc{\'\i}a-Osorio, C{\'e}sar},
journal = {Information Fusion},
year = {2021},
month = {oct},
volume = {74},
pages = {39-49},
issn = {1566-2535},
doi = {https://doi.org/10.1016/j.inffus.2021.03.007},
url = {https://www.sciencedirect.com/science/article/pii/S1566253521000634},
keywords = {Rotation Forest, Random Forest, Ensemble learning, Machine learning, Big Data, Spark},
publisher={Elsevier}
}
```
