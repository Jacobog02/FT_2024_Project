Jacob Gutierrez
Mar 5 2024


Installing CellPhone DB within a conda environment 

https://github.com/ventolab/CellphoneDB

```
conda create -n cpdb python=3.8

source activate cpdb

#https://stackoverflow.com/questions/41060382/using-pip-to-install-packages-to-anaconda-environment
conda install pip
#echo $CONDA_PREFIX ## see where conda path is 

#pip install cellphonedb
/home/jacobog/bin/miniconda3/envs/cpdb/bin/pip install cellphonedb


## Visualization 
/home/jacobog/bin/miniconda3/envs/cpdb/bin/pip install ktplotspy

#pip install -U ipykernel
conda install ipykernel

python -m ipykernel install --user --name 'cpdb'

## Open/Start Jupyter and select the created kernel
## HAD ISSUE: https://community.anaconda.cloud/t/jupyter-notebook-not-launching-from-anaconda/62535
pip uninstall traitlets
pip install traitlets==5.9.0

## Download the database via .ipynb 
```



