# Basic question: P(Hypo|DX)=? How to compare different hypotheses and make decision?
what I know: 
* Bayesian to combine D(data) and X(any knowledge)
* null VS alternative hypothesis: it's actually only about P(D|Hnull X), and usually assume some gaussian distribution of D (or alternatively, ranking tests)? There's no P(H|X).
what I want to know:
* how to incorporate P(H|X) to do hypo test? Also, in reality how to get P(H|X)?
*to check: Bayesian hypothesis testing*

# 4.2how to compare two hypothesis P(H1|DX) and P(H2|DX)?
## what quantity to describe how "probable" H1 over H2?
odds=P(H1|DX)/P(H2|DX)
### can we do some basic transformation to make it easier to calculate & intuitively sensible?
log of posterior. (Weber–Fechner law)
and 10-base log makes more intuitive sense => using *decibel*!
> equation (4.13)
### numerically how large will the evidence? how large would we think it's "overwhelming evidence"?
> Table 4.1
## example of using evidence test? bad machine problem
+ What's prior evidence?
+ What's the likelihood evidence? 
+ Especially, in the limit of infinite num of total samples, how much more evidence will a new sample provide?
*In the limit, good or bad widget don't share same level of loudness*. Bad widget more strongly biases towards bad machine than good widget towards good machine. 

**my Q:** to generalize, in what cases will this asymetry be strong?take p_h1(BAD) = k*p_h2(BAD), k increases, the BAD sample speaks louder for h1.

+ in the limit of initinite samples available, threshold to say h1 is more likely?
+ given posterior evidence, how to make decision (if accepting the hypothesis)?

# 4.3 from binary to multiple hypotheses
Assuming mutual exclusive Hs.
**my Q*: in applications with multiple hypotheses (ANOVA, fMRI, ...nested model comparison?), do we assume Hs are mutual exclusive?

# 4.4 multiple hypotheses testing
## What if all samples are BAD, should we firmly believe in H1?
No. Odds are high doesn't mean the likelihood itself is high. We are comparing between two really bad hypothesis, one's better than the other doesn't mean this one is good.
## How to test H1 VS ~H1 a.k.a. H2+H3?
### formulation?
Hard to use addition rule when H2+H3 on "condition" side => use Bayes.
Intuitively, (4.39) looks like likelihood of H2 and H3, weighted by their individual prior.
> alternative trick: 4.4.1, using product rule instead of addition rule to seperate A an dB

### numbers / trend?
> 4.46 & 4.47, from approximation on larger m and smaller m side. Do some basic algebra then you'll see it.
+ intuitivley what should it look like?
1) evidence of hypothesis C should be monotonically increase with m
2) more m, the increment should decrease (bc the evidence is already strong enough)
3) interestingly, evidence will accumulate linealry as m increases, instead of saturate...
+ so, when should we make decision (m=? will cross the threshold)?
linear apprx helps to get threshold!

### What about other 2 hypotheses? how do their evidence func change with m?
> see fig4.1
+ intuitively how to interpret them, or what are the features in this function?
1) all functions can be apprx by 2 linear funcs 
(*always like this for binary test?* -- no, only because there's 2 alternative H. these 2 approx are approxing relative evidence for the other 2 guys. If it's 3 alternative there should be 3 apprx. See below.)
2) interestingly, *curve slope change point* is related with *crossing point*!! Why is that? Simple explanation: crossing means the other H has become dominating, so slope of H' would be mainly depend on relative strength between this H and H'.
> to summarize: "a change in plausibility for any one of them will be approximately the result of a test of this hypothesis against a single alternative – the single alternative being that one of the remaining hypotheses which is most plausible at that time".
This way, **multiple hypo test reduces to binary test**.

+ how to summarize the decision result?
> flow chart Fig4.2, i.e. all possible binary tests.

** now, go back and play with problem setting ** 
### when would an unexpected hypothesis be resurrected?
problem 4.2 & 4.3, asking: general expression of threshold-unexpected probability setting? number of m to resurrect that dead hypothesis?










