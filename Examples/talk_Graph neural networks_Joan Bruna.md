my ques:
- why is graph model special? what kinda problem does it suit?
compare with normal deep learning: 1) need to formalize the inductive bias 2) need to generalize it

description of ml problem: x=x(u), u is intial euclidian high dimensional data; then output it to y=f(x).
what's special in this f(x)?
--should be a stable prior?

# what does stable mean?
||f(x)-f(x')|| should be smaller than a*||x-x'|| -- yet, there's the curse of dim that makes this not practical

## what t do?
x_t(u) = x(u-t(u)) -- using t(u) to do warping on the u
