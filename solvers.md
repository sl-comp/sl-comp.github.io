# Participants to SL-COMP

## Asterix
### Description
Asterix implements a model-based approach to decide separation logic
satisfiability and entailment queries. Our procedure, relying on SMT
solving technology to untangle potential aliasing between program
variables, has at its core a _matching_ function that checks whether a
concrete valuation is a model of the input formula and, if so,
generalises it to a larger class of models where the formula is also
valid. The version submitted to this competition is dynamically linked
with Z3 and implements support for the acyclic list segment predicate
only. Details about the algorithm and its correctness are described in

J. A. Navarro Perez and A. Rybalchenko. Separation Logic Modulo Theories.
In Proc. APLAS'13, 2013.

### Contact
   * Juan Antonio Navarro Pérez <juannavarroperez@gmail.com>
   * Andrey Rybalchenko <rybal@microsoft.com>

### Participation
   * 2014: **`sll0a_sat`**, /=sll0a_entl=/
   * 2018: /=qf_shls_sat=/, /=qf_shls_entl=/
   
