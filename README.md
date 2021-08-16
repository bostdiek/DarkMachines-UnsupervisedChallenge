# DarkMachines-UnsupervisedChallenge
[![DOI](https://zenodo.org/badge/364732311.svg)](https://zenodo.org/badge/latestdoi/364732311)
[![arXiv](https://img.shields.io/badge/arXiv-2105.14027-b31b1b.svg)](https://arxiv.org/abs/2105.14027)


## Abstract
We describe the outcome of a data challenge to detect signals of new physics at the LHC using unsupervised machine learning algorithms conducted as part of the
[Dark Machines initiative](https://www.darkmachines.org).
We first define and describe a large benchmark dataset, consisting of $>1$ Billion simulated LHC events corresponding to 10 fb^{-1} of proton-proton collisions at a center-of-mass energy of 13 TeV. We then review a wide range of anomaly detection and density estimation algorithms, developed in the context of the data challenge, and we measure their performance in a set of realistic analysis environments. We draw a number of useful conclusions that will aid the development of unsupervised new physics searches during the third run of the LHC, and provide our benchmark dataset for future studies at [phenoMLdata](https://www.phenoMLdata.org).

## Contents
Results for the Dark Machines Unsupervised Learning Challenge.

The `notebooks` directory contains jupyter notebooks for creating the figures in the paper for the results of the over 1000 models submitted for the challenge.

The individual results can be found in the `data` directory.
```
.
├── data/
│   ├── AE.csv
│   ├── ALAD.csv
│   ├── CNN_BVAE.csv
│   ├── CNN_VAE.csv
│   ├── Combined.csv
│   ├── ConvVAE_and_Flows.csv
│   ├── DAGMM.csv
│   ├── DarkMachinesUnsupervisedChallenge_TotalImprovements.csv
│   ├── DeepSetVAE.csv
│   ├── DeepSVDD.csv
│   ├── Flow.csv
│   ├── KDE.csv
│   ├── MethodsInLatentSpaceOfVAE.csv
│   ├── Metric_Scores.csv
│   ├── ModelsToSecretResults.csv
│   └── VAE.csv
├── figures/                  <- Figures from the paper
│   └── indivdual_signals/    <- Not included in the paper, contains best results for each BSM signal
├── LICENSE
├── notebooks/
│   ├── 01-ExampleBoxAndWhiskerPlot.ipynb
│   ├── 02-AnalysisAcrossPhysicsSignals_FigureOfMerit.ipynb
│   ├── 03-AnalysisOfTopMethodsForFiguresOfMerit.ipynb
│   ├── 04-SignificanceImprovement.ipynb
│   ├── 05-CompareWithSecretSetResults.ipynb
│   └── README.md
└── README.md
```

## Contributing new models
We encourage the development of new models using the Dark Machines datasets.
The easiest way to compare new models will be to add a CSV file to the `data` directory using the same formatting.
```
Signal,Model,Chan,AUC,1e-2,1e-3,1e-4
stop2b1000_neutralino300,YOURMODEL_NAME,1,0.87,0.21,0.10,0.05
...
monoV_Zp2000.0_DM_1.0,YOURMODEL_NAME,3,0.78,0.08,0.03,0.01
```
Then, rerun the notebooks and append the new file to the list being analyzed.

## bibtex citation
Please use the following bibtex citations if you use the data or notebooks from this study.
 * The article:
```
@article{Aarrestad:2021oeb,
    author = "Aarrestad, T. and others",
    title = "{The Dark Machines Anomaly Score Challenge: Benchmark Data and Model Independent Event Classification for the Large Hadron Collider}",
    eprint = "2105.14027",
    archivePrefix = "arXiv",
    primaryClass = "hep-ph",
    month = "5",
    year = "2021"
}
```
 * The code:
```
@software{bryan_ostdiek_2021_4897467,
  author       = {Bryan Ostdiek},
  title        = {{bostdiek/DarkMachines-UnsupervisedChallenge:
                   arXiv\_v1}},
  month        = jun,
  year         = 2021,
  publisher    = {Zenodo},
  version      = {0.2-alpha},
  doi          = {10.5281/zenodo.4897467},
  url          = {https://doi.org/10.5281/zenodo.4897467}
}
```
