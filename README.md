# Multiline Queues and some generalizations

The following files implement the objects and maps from "Macdonald polynomials at t = 0 through (generalized) multiline queues" (https://arxiv.org/abs/2407.05362, and we refer to this preprint as [MV24]). The multiline queues considered here are the t=0 version of the objects from "From multiline queues to Macdonald polynomials via the exclusion process" (https://muse.jhu.edu/pub/1/article/850573) where the authors introduce extra parameters to the multiline queues of Ferrari and Martin (https://www.jstor.org/stable/25449997) to make an explicit connection of multiline queues and Macdonald polynomials.

We give a quick description on how the fules are organized. 

## MultilineQueues and ExampleMLQs

In *MultilineQueues*, the class of these objects is created with the combinatorial features needed in the t=0 case. They include the definition of objects from ball arrangements, pairing and collapsing procedures, the statistics that give the connection to q-Whittaker polynomials, and an implementation of the RSK-esque algorithms defined on multiline queues. *ExamplesMLQs* contains different explicit examples, visualization of the objects, and instances of some of the methods. 

## GameMLQs

In the appendix of [MV24], we define an insertion algorithm on multiline queues to give an explicit bijection from MLQs and semistandard Young tableaux. This insertion algorithm always reminded me of Connect4. In *GameMLQs*, I implemented the game. 

### How to play

First, you choose the number of columns *C* in which you are going to play, and the board initializes in the empty board. Player1 has RED pieces, and Player2 has BLUE pieces. The players input numbers between 1 and *C* in order to insert a RED/BLUE piece in the given column. Such piece is inserted in the multiline queue (pairing weakly to the right) and the state of the board is always a non-wrapping MLQ. Similar to Connect4, the first player to have 4 pieces of their color in a row wins. 

## GeneralizedMultilineQueues and ExampleGMLQs

The objects whose class is defined in *GeneralizedMultilineQueues* correspond to the multiline queues from "Multiline Queues with Spectral Parameters" (https://link.springer.com/article/10.1007/s00220-020-03694-4). It contains the generalized pairing algorithm and the methods to compute the statistics from [MV24] to stablish the new formulas for q-Whittaker polynomials based on this objects. In the preprint, they are now called *Twisted Multiline Queues*. Once again, *ExamplesGMLQs* contains explicit calculations and visualization of the objects. 

## MultilineDiagrams and ExampleMLDs

In [MV24] we also consider a bosonic/plethystic analog of multiline queues that were originally called Multiline Diagrams. In more recent versions of the preprint, they are called *Bosonic Multiline Queues*. In *MultilineDiagrams*, the class of the objects is defined with the construction from bosonic ball arrangements, pairing and collapsing procedures, and the statistics that stablish their connection with the evaluation of modified Hall--Littlewood polynomials at t=0. Once again, *ExamplesMDQs* contains explicit calculations and visualization of the objects. 

# Generalizations of Multiline Queues

While Twisted and Bosonic multiline queues are generalizations of the multiline queues from Ferrari and Martin, they have algebraic motivation arising from the combinatorial R-matrix and plethystic identities of the Macdonald Polynomials respectively. The following files include generalizations motivated from other sources.

## SupersymmetricMultilineQueues and ExampleSuperMLQs

We can consider multiline queues in which columns can be fermionic or bosonic. We can make the pairing direction match and generalize the pairing algorithm from Bosonic and (Fermionic) multiline queues. *SupersymmetricMultilineQueues* has the class of objects that we call *Supersymmetric* since they are in bijection with supersymmetric semistandard tableaux (see "A Determinantal Formula for Supersymmetric Schur Polynomials" (https://link.springer.com/article/10.1023/A:1025048821756) for the connection of these objects with representation theory of Lie Superalgebras.) 

## PosetMultilineQueues

...

