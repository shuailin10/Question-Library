my ques:
- why is graph model special? what kinda problem does it suit?
compare with normal deep learning: 1) need to formalize the inductive bias 2) need to generalize it
from the examples about LHC, it seems able to learn about theories (=inductive bias)!
is its trained parameters more interpretable?
- (I haven't understood): why is this stability thing critical (it's a driven factor for gnn model construction?). does that correspond to some human cognition intuition?


# euclidean geometric stability -- start with well worked out CNN
## phrase the problem
x=x(u), u is intial euclidian high dimensional data; then output it to y=f(x).
what's special in this f(x)?
--should be a stable prior?

## what does stable mean? why is that important?
||f(x)-f(x')|| should be smaller than a*||x-x'|| -- yet, there's the curse of dim that makes this not practical

## consider using deformation to redefine stability
x_t(u) = x(u-t(u)) -- using t(u) to do warping on the u
--**deformation**
and stability means even under deformation there's some invariability

## relation with cnn? why are cnns geometrically stable? 
**demo of why this stability idea is critical to a successful algorithm**
local kernel is similar to local translation/deformation...(lead to multiscale architechture??)
convulutions to exploit translation invariance/equivariance

# what if input data is non-euclidean gemoetries? -- graph neural network
## exmaples
social network
and...?
(high energy physics, need to learn the physical interactions)
```my intuition: graph model suits for highly interactive variables? what kinda data is it good for, after all??```

## phrase the problem
using a graph to represent x(u)
## what is geometric deformation in graph?
-transform into low-dim euclidean embedding...correspondence...
-distance between graphs (defined by some metrics)
## what is geometric stability priors in graph?
analogy: we want localized, multiscale filters in euclidean space => linear diffusion operators, localized operator (local smoothing)
also it's stable (can be shown).

~low-pass filter [??]

## actual algorithm implementation?
utilizing laplacian (??)
- spectral networks (Bruna et al 2014)
many other GNN implementations!

### what can they do?
high energy physics: able to determines the parameters of physical interaction thru the trained kernels...
```interesting!! could we use that in "theory generation"?```

# another Q: statistical inference on graphs 
so input data is graph itself.

2 main algorithm frameworks:
+ fraph conductance/min-cut approach->spectral clustering algorithms
+ probabilistic graph models -> belief propagation
or mix them together

yet how to learn the algorithm itself?




