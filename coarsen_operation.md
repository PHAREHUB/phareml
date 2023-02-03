# Coarsen Operation

When doing a coarsen operation between two patches (the source will be the fine patch, and the destination the coarse patch),
the fine patch is guarenteed to contain sufficient data for the stencil width of the coarsening operator (ie: the number of point 
needeed in the source to coarse the data on one point of the destination).
To perform the coarsening, we will have to first choose how much point wee need.
Depending on the centering, this number may change :

For example using spline of order from 1 to 3, possibles number of point in function
of the centering

| centering | order 1 | order 2 | order 3 |
| --        |      -- | --      | --      |
| dual      |       2 | nop     | 4       |
| primal    |       1 | 3       | nop     |
|           |         |         |         |
