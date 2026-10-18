# Unit 8: Gradient Descent and the Cost Function

## Activity objective

This activity explored how the number of iterations and the learning rate affect gradient descent when fitting a linear regression model. The objective was to reduce the cost function while moving the model parameters towards suitable values.

The notebook used the data points \(x=[1,2,3,4,5]\) and \(y=[5,7,9,11,13]\), with the model \(y=mx+b\). The initial slope and intercept were both zero.

## Experiment 1: Reducing the number of iterations

The first experiment used a learning rate of 0.08 and reduced the number of iterations from 100 to 10.

| Measure | Result |
|---|---:|
| Learning rate | 0.08 |
| Iterations | 10 |
| Initial printed cost | 89.0 |
| Final printed cost at iteration 9 | 12.0468 |
| Slope printed at iteration 9 | 1.6309 |
| Intercept printed at iteration 9 | 1.0383 |

The cost decreased from 89.0 to 12.0468. This indicates that the algorithm was reducing prediction error, but ten iterations did not bring the parameters close to the underlying relationship \(y=2x+3\).

## Experiment 2: Reducing the learning rate

The second experiment used 100 iterations and reduced the learning rate from 0.08 to 0.01.

| Measure | Learning rate 0.08 | Learning rate 0.01 |
|---|---:|---:|
| Iterations | 100 | 100 |
| Initial printed cost | 89.0 | 89.0 |
| Last printed cost at iteration 99 | 0.00412 | 0.48041 |

With the learning rate of 0.01, the cost decreased more gradually and remained higher after 100 iterations than in the original run. In this experiment, the learning rate of 0.08 reached a lower cost more quickly.

## Interpretation and limitations

The experiments demonstrated that gradient descent performance depends on both the number of iterations and the learning rate. Too few iterations may leave the model insufficiently optimised, while a smaller learning rate may require more iterations to make comparable progress. A learning rate that is too high can cause unstable updates or divergence.

The notebook calculates the cost before updating the parameters in each iteration, then prints the updated slope and intercept alongside that cost. Therefore, the printed cost and printed parameters do not correspond to exactly the same point in the optimisation process.

## Reflection

This activity helped me connect the mathematical idea of optimisation with observable changes in a model's cost. I learned that model training involves choices about how far parameters move during each update and how long optimisation continues. These choices should be evaluated using observed behaviour rather than assumptions.

This understanding is relevant to my TrashNet assignment, where model development and fine-tuning influenced the evaluation process. In future experiments, I will document parameter settings, compare results systematically and use validation data for model selection while keeping the test set independent for final evaluation.

## Evidence

The results on this page were recorded from the Unit 8 gradient-descent notebook. The baseline experiment used 100 iterations with a learning rate of 0.08; the two subsequent experiments changed the iteration count and learning rate as described above.
