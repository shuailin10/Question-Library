## what is err-backprop?
The way to adjust layer weights / signal transformations to make the output have less error.
An extension: continuous time domain. differential eq

## neural implementation?
### where is the top-down signal (Back props the error value)?
classically: from pyramidal dentrites, and will modulate gains for bottom-up input
new: err prop in apical tre (error comparison there) via SOM interneurons => two pyramidal neurons are involved (1 receives top-down signal then props to interneuron, which manipulates the gain of the 2nd pyramidal neuron that deals with sensory bottom up signals)
Specifically, the somatic voltage is like storing the previous answer, and being taught by the input soma.

## What i've learnt:
- error-backprop is easily connected to neuron network structures 
(excites/inhibits of neurons; each operation could be mapped to a neuron type)
- this backprop should be able to optimize some output 
(shown by 1: working on real data like NMIST; 2: equivalence to gradient decendent (or any proved algorithms that does correct optimization)

