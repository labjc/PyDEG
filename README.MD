PyDEG is a python implementation of the differential expression analysis(DEA) with bulk RNA-seq data. You have to note that it is just a mimic of DESeq2 of python and DESeq2 of R. We are neither majors nor experts. 

Please refer to the following links : https://github.com/owkin/PyDESeq2 & https://hbctraining.github.io/DGE_workshop/lessons/04_DGE_DESeq2_analysis.html

Currently, PyDEG uses median of ratios as the size factors, like DESeq2. However, there are many differeces between PyDEG and DESeq2(or PyDESeq2). For instance, We use the likelihood-ratio test unlike DESeq2 which mainly uses the wald test.

There may be many errors and the code may reflect things we know are wrong. We will fix these things. If you notice anything strange, please feel free to contact me at any time.

## Contents

1. Installation
2. How to use
3. License

---
## Installation
PyDEG can be installed from PyPI using pip
```
pip install PyDEG
```

---
## How to use
Import pydeg_dataset and results from pydeg. You may need import pandas.
```python
import pandas as pd
from pydeg.pdd import pydeg_dataset, results
```
Create pydeg_dataset object where count_data is a pandas.DataFrame containing raw counts, metadata is a pandas.DataFrame containing information about samples and the design is string design formula.
```python
pdd = pydeg_dataset(count_data, metadata, design)
```
Estimate size factors, dispersinos and fit GLM for each gene.
```python
pdd.DEA()
```
Test for differential expression with contrast = [condition, control, treat]
```python
res = results(pdd, contrast)
```

