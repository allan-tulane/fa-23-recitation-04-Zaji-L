# CMPS 2200 Reciation 5
## Answers

**Name:** Charlie Landman


Place all written answers from `recitation-05.md` here for easier grading.







- **1b.**
quick sort with fixed pivot is always quicker than quick sort with random pivot and both are always quicker than selection sort because O(nlogn) is much quicker than O(n^2). For the most part, fixed pivot is much more predictable and useally faster, but there can be cases where random pivot (randomly) is quicker. With smaller list sizes, selection sort is faster.
|     n |   qsort-fixed-pivot |   qsort-random-pivot |    ssort |
|-------|---------------------|----------------------|----------|
|   100 |               0.174 |                0.362 |    0.068 |
|   200 |               0.370 |                0.544 |    0.046 |
|   300 |               0.512 |                1.499 |    0.130 |
|   500 |               1.212 |                1.928 |    0.106 |
|  1000 |               5.253 |                5.960 |    0.309 |
|  5000 |              47.436 |               96.161 |    4.348 |
|  1000 |               3.319 |                6.306 |    1.444 |
| 10000 |              97.352 |              114.136 |    4.709 |
| 20000 |             179.704 |              218.545 |  141.371 |
| 50000 |             417.709 |              527.348 | 3303.574 |
in this case, we can see that at the largest value, ssort balloened in rumtime, which makese sense considering it's quadratic runtime.
|      n |   qsort-fixed-pivot |   qsort-random-pivot |    ssort |
|--------|---------------------|----------------------|----------|
|    100 |               0.556 |                0.495 |    0.080 |
|    300 |               1.046 |                1.344 |    0.120 |
|    500 |              33.717 |                2.528 |    2.257 |
|   1000 |               3.246 |                5.818 |    0.271 |
|   2000 |               7.529 |               13.594 |    0.535 |
|   5000 |              20.324 |               68.581 |    2.685 |
|  10000 |              89.502 |              100.686 |    3.572 |
|  20000 |             176.236 |              242.343 |  341.495 |
|  50000 |             435.807 |              606.951 | 3554.293 |
| 100000 |             980.402 |             1566.002 | 6650.615 |
here is a table with higher numbers



- **1c.**
|      n |   qsort-fixed-pivot |   timesort |
|--------|---------------------|------------|
|    100 |               0.296 |      0.004 |
|    300 |               0.624 |      0.008 |
|    500 |               2.108 |      0.009 |
|   1000 |               1.971 |      0.011 |
|   2000 |               4.886 |      0.023 |
|   5000 |              11.604 |      0.050 |
|  10000 |              76.454 |      0.097 |
|  20000 |             126.127 |      0.347 |
|  50000 |             459.540 |      1.198 |
| 100000 |             991.865 |      1.336 |

timesort is much faster