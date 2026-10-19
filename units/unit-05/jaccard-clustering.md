# Unit 5: Jaccard Distance and Dissimilarity

## Activity Overview

This activity explored the use of Jaccard distance to measure dissimilarity between individuals using categorical pathological test results. The task was to calculate the distance between three pairs: Jack and Mary, Jack and Jim, and Jim and Mary.

## Method

Jaccard distance is calculated as:

dj (A,B) = 1 – M11/ (M11 + M10 + M01 )

Where:

- \(M_{11}\) represents attributes where both individuals have a positive value.
- \(M_{10}\) represents attributes where the first individual has a positive value and the second does not.
- \(M_{01}\) represents attributes where the second individual has a positive value and the first does not.

Shared negative values are excluded from the calculation.

**Assumption:** The original activity does not define the meanings of `P` and `A`. For these calculations, `Y` and `P` are treated as positive values, while `N` and `A` are treated as non-positive values. Gender is excluded because the calculation focuses on the recorded symptoms and test results.

## Calculations

### 1. Jack and Mary

Comparing Fever, Cough and Test-1 to Test-4:

- Shared positive attributes: Fever and Test-1.
- Total attributes positive for at least one individual: Fever, Test-1 and Test-3.

Therefore:

\[
d_J(\text{Jack, Mary})=1-\frac{2}{3}
=\boxed{0.333}
\]

### 2. Jack and Jim

- Shared positive attribute: Fever.
- Total attributes positive for at least one individual: Fever, Cough and Test-1.

Therefore:

\[
d_J(\text{Jack, Jim})=1-\frac{1}{3}
=\boxed{0.667}
\]

### 3. Jim and Mary

- Shared positive attribute: Fever.
- Total attributes positive for at least one individual: Fever, Cough, Test-1 and Test-3.

Therefore:

\[
d_J(\text{Jim, Mary})=1-\frac{1}{4}
=\boxed{0.750}
\]

## Summary of Results

| Pair | Jaccard distance | Interpretation |
|---|---:|---|
| Jack and Mary | 0.333 | Most similar under the stated assumption |
| Jack and Jim | 0.667 | Greater dissimilarity |
| Jim and Mary | 0.750 | Most dissimilar under the stated assumption |

A Jaccard distance closer to zero indicates greater similarity, while a value closer to one indicates greater dissimilarity.

## Learning and Findings

This activity helped me understand how a similarity measure can compare records containing categorical attributes. The results showed how shared positive attributes and differences between records influence the calculated distance.

The activity also highlighted the importance of understanding and encoding data correctly before applying machine-learning techniques. In healthcare-related datasets, ambiguous category labels can affect similarity calculations and potentially lead to misleading interpretations. The meanings of the recorded values should therefore be confirmed before the results are used to support decisions.

## Evidence

The original activity table and the calculations above document the exercise. The calculations are based on an explicit working assumption because the original instructions do not define `P` and `A`.
