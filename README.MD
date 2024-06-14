PyDEG is a python implementation of the differential expression analysis(DEA) with bulk RNA-seq data. You have to note that it is just a mimic of DESeq2 of python and DESeq2 of R. We are neither majors nor experts. 

Please refer to the following links : https://github.com/owkin/PyDESeq2 & https://hbctraining.github.io/DGE_workshop/lessons/04_DGE_DESeq2_analysis.html

Currently, PyDEG uses median of ratios as the size factors, like DESeq2. However, there are many differeces between PyDEG and DESeq2(or PyDESeq2). For instance, We use the likelihood-ratio test unlike DESeq2 which mainly uses the wald test.

There may be many errors and the code may reflect things we know are wrong. We will fix these things. If you notice anything strange, please feel free to contact me at any time.
