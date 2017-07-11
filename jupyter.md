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

## Draw 3d array as plot using matplotlib
```
import matplotlib.pyplot as plt, numpy as np
from mpl_toolkits.mplot3d import Axes3D

v= np.array([[1,2,3], [4,5,6], [7,8,9]])
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot(v[:,0],v[:,1],v[:,2])
plt.show()
```
