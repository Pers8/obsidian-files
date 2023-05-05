Let's consider the following grid/matrix:
```md
[ 1  0  1  2  0]
[ 2  1  0  1  0]
[ 0  0  2  0  1]
[ 1  2  1  0  2]
[ 0  1  0  2  1]

```

Suppose we want to extract features from this matrix using a convolutional layer with a filter of size 3x3. To do this, we would slide the filter over the input matrix, multiplying each element of the filter with the corresponding element in the input matrix and then summing the results to produce a single output value.

For example, let's consider the position in the top left corner of the input matrix, which corresponds to the sub-matrix: