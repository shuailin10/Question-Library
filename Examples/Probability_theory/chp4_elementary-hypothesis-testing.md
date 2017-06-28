# Basic question: P(Hypo|DX)=? How to compare different hypotheses and make decision?
what I know: 
* Bayesian to combine D(data) and X(any knowledge)
* null VS alternative hypothesis: it's actually only about P(D|Hnull X), and usually assume some gaussian distribution of D (or alternatively, ranking tests)? There's no P(H|X).
what I want to know:
* how to incorporate P(H|X) to do hypo test? Also, in reality how to get P(H|X)?
*to check: Bayesian hypothesis testing*

# how to compare two hypothesis P(H1|DX) and P(H2|DX)?
## what quantity to describe how "probable" H1 over H2?
odds=P(H1|DX)/P(H2|DX)
### can we do some basic transformation to make it easier to calculate & intuitively sensible?
log of posterior. (Weber–Fechner law)
and 10-base log makes more intuitive sense => using *decibel*!
> equation (4.13)
### numerically how large will the evidence? how large would we think it's "overwhelming evidence"?
> Table 4.1
## example of using evidence test?






