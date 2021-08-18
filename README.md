# Single-cell Analysis Tutorial

## About

![image](https://drive.google.com/uc?export=view&id=1YoX3F8gNGH5K0AFu4wFdd5ccEXT-mP_J)

This repository is complementary to the publication:

M.D. Luecken, F.J. Theis, "Current best practices in single-cell RNA-seq analysis: a tutorial", Molecular Systems Biology 15(6) (2019): e8746

The paper was recommended on F1000 prime as being of special significance in the field.

<a href="https://f1000.com/prime/736010853?bd=1 &ui=150648 " target="_blank"><img src="https://s3.us-east-1.amazonaws.com/cdn.f1000.com/images/badges/badgef1000.gif" alt="Access the recommendation on F1000Prime" id="bg" /></a>

The corresponding book is hosted [here](https://github.com/theislab). The main part of the book is dedicated to a case study where the best-practices established in our manuscripts are applied to a mouse intestinal epithelium regions dataset from Haber et al., Nature 551 (2018) available from GEO under GSE92332.
Specific topics such as RNA velocity use other datasets as noted in the book.
Moreover, the book contains many teaching resources such as quizzes with solutions.

## Contributing

We would like to invite the community to further improve the tutorial and the teaching material.
Please read [contributing](contributing.md) for further instructions.

In case of questions or issues, please get in touch by posting an issue in this repository.

If the materials in this repository are of use to you, please consider citing the above publication.

## Adapting the notebooks to other datasets:

All notebooks for the various steps can be found in the [notebooks folder](single-cell-best-practices/tree/master/notebooks). 
These can easily be reused for your own projects.
Please note that there are several limitations to the general applicability of the current workflow. When adapting the pipeline for your own dataset please take into account the following:

1. Sparse data formats are not supported by `rpy2` and therefore do not work with any of the integrated R commands. Datasets can be turned into a dense format using the code: `adata.X = adata.X.toarray()`

2. The case study assumes that the input data is count data obtained from a single-cell protocol with UMIs. If the input data is full-length read data, then one could consider replacing the normalization method with another method that includes gene length normalization (e.g., TPM).

## Acknowledgements

This tutorial would not be possible without the input of all Theislab members and the countless benchmarks and reviews of various single-cell tools by the community. Furthermore, the tutorial book's technical backend was adapt from the [scikit-learn-mooc](https://github.com/INRIA/scikit-learn-mooc).
