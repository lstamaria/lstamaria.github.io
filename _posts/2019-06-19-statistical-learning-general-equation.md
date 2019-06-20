A general equation of statistical learning involves four elements.  These are:

- Response (Y): what want to predict quantitatively. It is also called as a target feature.
- Predictor (X): what we use to estimate a response. It is also called as a descriptive feature.
- Function (f): a systematic information that predictor provides to response. It is fixed but unknown. 
- Error ($\epsilon$): element that refers to random error independent of predictor.

![](assets/image/20190620/response_predictor.png)

In equation form:

\begin{equation}\label{relXY}
Y = f(X) + \epsilon
\end{equation}

where

- $Y$ is response
- $X$ is predictor
- $f$ is function 
- $\epsilon$ is error

## Reference

James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). An Introduction to Statistical Learning (Vol. 103). https://doi.org/10.1007/978-1-4614-7138-7

## Appendix

### Source Code


```python
# Import supporting packages

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.datasets import make_regression
from numpy.polynomial.polynomial import polyfit
```


```python
# Generate data points

sample_size = 100
dataset = make_regression(sample_size, 1, noise=20, random_state=42)
dataset = pd.DataFrame({'X':dataset[0].reshape(1, sample_size)[0], 'Y':dataset[1]})
dataset.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>X</th>
      <th>Y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.931280</td>
      <td>62.687202</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.087047</td>
      <td>-23.763981</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-1.057711</td>
      <td>-25.686766</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Plot data pooints

fig, ax = plt.subplots(1, 1, figsize=(4, 3), dpi=72*2)

ax.scatter(dataset.X, dataset.Y, color='b', marker='.')

b_coeff, m_resid = polyfit(dataset.X, dataset.Y, 1)
ax.plot(dataset.X, m_resid*dataset.X + b_coeff, color='r')

ax.set_xlabel('X')
ax.set_ylabel('Y')
fig.tight_layout();
fig.savefig('asset/response_predictor.png');
plt.close(fig);
```
