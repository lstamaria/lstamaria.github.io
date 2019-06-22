


A general equation of statistical learning involves four elements (James, et al., 2013).  These are:

- Response (Y): what want to predict quantitatively. It is also called as a target feature.
- Predictor (X): what we use to estimate a response. It is also called as a descriptive feature.
- Function (f): a systematic information that predictor provides to response. It is fixed but unknown. 
- Error ($\epsilon$): term that refers to random error independent of predictor.

![png](/assets/images/20190619/response_predictor.png)

In equation form:

\begin{equation}\label{eq_statlearning}
Y = f(X) + \epsilon
\end{equation}

where

- $Y$ is response
- $X$ is a set of predictors
- $f$ is function 
- $\epsilon$ is error term

Equation \ref{eq_statlearning} shows the elements of statistical learning.


I used the Python code below to produce the graph.


```python
# Import supporting packages
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.datasets import make_regression
from numpy.polynomial.polynomial import polyfit

# Generate data points
sample_size = 100
dataset = make_regression(sample_size, 1, noise=20, random_state=42)
dataset = pd.DataFrame({'X':dataset[0].reshape(1, sample_size)[0], 'Y':dataset[1]})

# Plot graph
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


## Reference

James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). An Introduction to Statistical Learning (Vol. 103). https://doi.org/10.1007/978-1-4614-7138-7