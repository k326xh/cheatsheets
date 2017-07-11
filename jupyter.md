# Jupyter notebook

Helpful tips for jupyter notebook

## Installing kernels from other environments

To install a kernel from another environment to your primary jupyter notebook, do this:

```
source activate myenv
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
source activate other-env
python -m ipykernel install --user --name other-env --display-name "Python (other-env)"
```

## Turn off known warnings in one cell
Codes need to be indented as the warnings.simplefilter() line
```
with warnings.catch_warnings():
    warnings.simplefilter("ignore")
```
