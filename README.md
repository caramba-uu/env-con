# Untargeted screening of environmental contaminants in human plasma using liquid chromatography high resolution mass spectrometry with negative ionization


In this paper, we developed a method to detect and identify both endogenous and exogenous compounds correlating with environmental contaminants in the body using mass-spectometry in untargeted mode.

---

## Setting up the environment
To create and activate the environment with necessary library and packages. <br>
```bash
conda env create -f environment.yaml
conda activate envcon
```
To process the files nextflow workflow [nf-core-metabolinden](https://github.com/PayamEmami/nf-core-metabolinden) was used. Install the workflow in the newly created environment.

---

## File descriptions
The parameter files for the FeatureFinder is [FF_param.ini](supp_files/FF_param.ini) and for FeatureLinker is [FL_param.ini](supp_files/FL_param.ini).  
The command used for the nextflow workflow can be found [here](supp_files/metabolinden_command.txt).  
The data needed for identification using m/z is available at [NORMAN database](https://www.norman-network.com/nds/susdat/)  

---

## Data preprocessing
1. [0_tracefinder_analysis.ipynb](python_notebooks/0_tracefinder_analysis.ipynb)  <br>
    * Plotting the correlation plot for result from TraceFinder. <br><br>
2. [1_feature_linker_coverage_check.ipynb](python_notebooks/1_feature_linker_coverage_check.ipynb)  <br>
    * Analysing and obtaining feature of native compounds from FeatureLinker <br><br>
3. [2_correlation_analysis.ipynb](python_notebooks/2_correlation_analysis.ipynb)  <br>
    * Plotting the correlation plot for result from FeatureFinder and FeatureLinker. <br><br>
4. [3_clustering.ipynb](python_notebooks/3_clustering.ipynb)  <br>
    * Clustering of features using coverage and correlation cutoff. <br><br>
5. [4_Identification.ipynb](python_notebooks/4_Identification.ipynb)  <br>
    * Identification of features using m/z using NORMAN database. <br><br>
6. [5_ms2_extraction.ipynb](python_notebooks/5_ms2_extraction.ipynb)  <br>
    * Extracting MS2 for the selected features and running CSI-FINGERID. <br><br>
7. [6_post_CSI_consolidate_results.ipynb](python_notebooks/6_post_CSI_consolidate_results.ipynb)  <br>
    * Extracting and analysing CSI-FINGERID results. <br><br>


---

## Acknowledgements and references

We thank everyone who helped us in the project.  
Special thanks to nf-core-metabolinden for the workflow.

---

## Citation
  
Please cite:  
Carlsson, Henrik & Sreenivasan, Akshai & Erngren, Ida & Larsson, Anders & Kultima, Kim. (2023). Combining targeted and untargeted screening of environmental contaminants reveals associations between PFAS exposure and vitamin D metabolism in human plasma. Environmental Science: Processes & Impacts. 25. 10.1039/D3EM00060E.
<br>

