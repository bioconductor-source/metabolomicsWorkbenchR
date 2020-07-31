
<!-- badges: start -->
[![Travis build status](https://travis-ci.com/computational-metabolomics/metabolomicsWorkbenchR.svg?branch=master)](https://travis-ci.com/computational-metabolomics/metabolomicsWorkbenchR)
[![AppVeyor build status](https://ci.appveyor.com/api/projects/status/github/computational-metabolomics/metabolomicsWorkbenchR?branch=master&svg=true)](https://ci.appveyor.com/project/RJMW/metabolomicsWorkbenchR)
[![Codecov test coverage](https://codecov.io/gh/computational-metabolomics/metabolomicsWorkbenchR/branch/master/graph/badge.svg)](https://codecov.io/gh/computational-metabolomics/metabolomicsWorkbenchR?branch=master)
<!-- badges: end -->

# metabolomicsWorkbenchR 
A Bioconductor package for interfacing with the Metabolomics Workbench API (https://www.metabolomicsworkbench.org/).

## Installation
To install from github use the `remotes` package, where `master` can be replaced with release tags if desired:
```{r}
remotes::install_github('computational-metabolomics/metabolomicsWorkbenchR@master')
```

## Introduction
This package enables access to the Metabolomics Workbench API (MWA) using a simple query interface. For example, the 'study' context can be queried using the 'study_title' input to search the database for all studies with the keyword 'Disease' in the title and return a study:

```{r}
library(metabolomicsWorkBench)
df = do_query(context = 'study', input_item = 'study_title', input_value = 'Diabetes', output_item = 'summary')
```

The query interface is designed to mirror the API documentation as closely as possible (https://www.metabolomicsworkbench.org/tools/MWRestAPIv1.0.pdf). All api endpoints are accessible via metabolmicsWorkbenchR. 
