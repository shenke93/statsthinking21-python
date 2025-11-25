Model: summarize data to provide a compact overivew.

Statistical model:
- Capture the structure of data as simply as possible.
- Most efficient and accurate summary.
- Basic structure:
  $$ data = model + error $$ 
- For the predicted value of observation $i$, the error is:
  $$ error_i = data_i - \widehat{data_i}$$
- Parameters: values that we can change in order to modify the predictions of the model.

Statistical modelling example: building a model of the height of children in the NHANES sample.
- Simplest model: using a single parameter $y_i = \beta + \epsilon$
  - How could we best estimate $\beta$?
  - Using average can give us an average error of zero
    $$ error = \sum_{i=1}^{n}(x_i - \bar{x}) \\
    = \sum_{i=1}^{n}x_i - n\bar{x} \\
    = \sum_{i=1}^{n}x_i - n\frac{1}{n} \sum_{i=1}^{n} x_i \\
    = 0 $$
  - We want to count both positive and negative errors as bad, metric selection: sum of squared errors (SSE), mean squared error (MSE), root mean squared error (RMSE). 
- Linear model: $\hat{y_i} = \hat{\beta_0} + \hat{\beta_1} * age_i$
  - Try different combinations: age, age+constant, age+constant+gender

What makes a model good:
- Lower the error:
  - Error comes from model.
  - Error comes from random variation in the data (even when the model is correct), measurement error or noise.
- Generalize to new data:
  - Overfitting.

Summarizing data
- Mean: 'central tendency' of the dataset.
  - Mean of a sample: 
  $$ \bar{X} = \frac{\sum_{i=1}^{n}x_i}{n} $$
  - Mean of a population, where $N$ is the size of the entire population
  $$ \mu = \frac{\sum_{i=1}^{N}x_i}{N} $$
- Median
- Mode
- Variance: 'variability' of the dataset.
  - Population variance, same as MSE:
  $$ \sigma^2 = \frac{SSE}{N} = \frac{\sum_{i=1}^{N}(x_i - \mu)^2}{N}$$
  - Population standard deviation, same as RMSE: $\sigma$
  - Sample variance: using $n-1$ because of the degree of freedom:
  $$ s^2 = \frac{\sum_{i=1}^{n}(x_i - \bar{X})^2}{n-1}$$
  - Sample standard deviation: $s$.