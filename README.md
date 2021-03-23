# Rotation Forest for Big Data

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

This work was supported through project TIN2015-67534-P (MINECO/FEDER, UE) of the *Ministerio de Economía y Competitividad* of the Spanish Government, project BU085P17 (JCyL/FEDER, UE) of the *Junta de Castilla y León* (both projects co-financed through European Union FEDER funds), and by the *Consejería de Educación* of the *Junta de Castilla y León* and the European Social Fund through a pre-doctoral grant (EDU/1100/2017). The project leading to these results has received also funding from "la Caixa" Foundation, under agreement LCF/PR/PR18/51130007. This material is based upon work supported by Google Cloud.

## Citation policy

The paper is currently accepeted on Information Fusion journal, and pending of publication. Citation policy will be updated as soon as it is published.