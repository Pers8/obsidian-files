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

```md
[ 1  0  1]
[ 2  1  0]
[ 0  0  2]
```

To process this sub-matrix through the convolutional layer, we would multiply each element of the filter with the corresponding element in the sub-matrix, and then sum the results :

```md
filter:      sub-matrix:
 1  0  1     1  0  1
 0  1  0     2  1  0
 1  0  1     0  0  2

result: 1*1 + 0*0 + 1*1 + 0*2 + 1*1 + 0*0 + 1*0 + 0*1 + 1*2 = 4

```

This produces a single output value of 4 for this position in the feature map.

We would repeat this process for each position in the input matrix, sliding the filter over the input matrix and computing the corresponding output value for each position. The resulting output matrix would then represent the feature map for that particular filter.