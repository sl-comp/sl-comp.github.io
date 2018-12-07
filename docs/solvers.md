
Participants to SL-COMP
=======================

# Asterix

Asterix implements a model-based approach to decide separation logic
satisfiability and entailment queries. Our procedure, relying on SMT
solving technology to untangle potential aliasing between program
variables, has at its core a _matching_ function that checks whether a
concrete valuation is a model of the input formula and, if so,
generalises it to a larger class of models where the formula is also
valid. The version submitted to this competition is dynamically linked
with Z3 and implements support for the acyclic list segment predicate
only. Details about the algorithm and its correctness are described in

* Reference
   * J. A. Navarro Perez and A. Rybalchenko. Separation Logic Modulo Theories.
In Proc. APLAS'13, 2013.

* Contact
   * Juan Antonio Navarro Pérez <juannavarroperez@gmail.com>
   * Andrey Rybalchenko <rybal@microsoft.com>

* Participation
   * 2014: `sll0a_sat`, `sll0a_entl`
   * 2018: `qf_shls_sat`, `qf_shls_entl`


# ComSPEN

ComSPEN (for Compositional SPEN) is a solver for the symbolic heap
fragment of SL with compositional ID. It also supports linear integer
arithmetics.

* Contact
   * Zhilin Wu <wuzl@ios.ac.cn>
   * Chong Gao <gaochong@ios.ac.cn>

* Participation
   * 2018 (expected but pull out for issue on StarExec): `qf_shidlia_sat`, `qf_shidlia_entl`,
   `qf_shlid_entl`, `qf_shls_entl`, `qf_shls_sat`
 
 
# Cyclist-SL

An entailment prover for separation logic with inductive predicates
based on cyclic proof.  The theory and design is described in

It includes SLSAT, a prover for satisfiability.

* Contact
   * Nikos Gorogiannis <nikos.gorogiannis@gmail.com>

* References
   * J. Brotherston, N. Gorogiannis, and R. L. Petersen. A generic cyclic
theorem prover. In Proc. APLAS-10, pages 350-367. Springer, 2012.


* Participation
   * 2014: /=UDB_entl=/, /=UDB_sat=/, /=sll0a_entl=/, /=sll0a_sat=/, /=FDB_entl=/
   * 2018: /=qf_shid_entl=/, /=qf_shid_sat=/,
   /=qf_shls_entl=/, /=qf_shls_sat=/, /=qf_shlid_entl=/,
   /=shid_entl=/


# CVC4

CVC4-SL includes a procedure for the boolean combination of
SL atoms without inductive definitions.

* Contact
   * Andrew J. Reynolds <andrew.j.reynolds@gmail.com>

* Participation
   * 2018: /=qf_bsl_sat=/, /=bsl_sat=/


# Harrsh

HARRSH is a prover for symbolic heap separation logic with user defined predicates. It can prove satisfiability as well as various reachability based properties of symbolic heaps, including garbage freedom and acyclicity. HARRSH is based on Heap Automata, as introduced in our ESOP 2017 paper, Unified Reasoning about Robustness Properties of Symbolic Heap Separation Logic.

* Contact
   * Jens Katelaan <jkatelaan@forsyte.at>

* Participation
   * 2018: /=qf_shid_sat=/, /=qf_shls_sat=/


# S2S

S2S is a Solver for Second-order Separation logic. It supports
constraints in separation logic combining with
general inductive definitions, arithmetic and string.
S2S includes a central component of a generic cyclic proof framework.
Currently, three cyclic-proof instantiations have been implemented:
two solvers of separation logic (one for satisfiability and one for entailment)
and one satisfiability solver of string logic.

* Contact
   * Le Quang Loc <lequangloc@gmail.com>

* Participation
   * 2018: /=qf_shid_entl=/, /=qf_shid_sat=/,
                /=qf_shidlia_entl=/, /=qf_shidlia_sat=/,
                /=qf_shls_entl=/, /=qf_shls_sat=/,
                /=shid_entl=/, /=shidlia_entl=/

# Sleek

* Contact
   * Benedict Lee <benedictleejh@gmail.com>
   * Chin Wei Ngan <chinwn@comp.nus.edu.sg>

* Participation
   * 2014: all
   * 2018: all


# Slide

SLIDE is a tool for deciding entailments between two given predicates,
from a larger system of inductively defined predicates, written in an
existential fragment of Separation Logic. The proof method relies on
converting both the left hand and right hand sides of the entailment
into two tree automata AutLHS and AutRHS, respectively, and checking
the tree language inclusion of the automaton AutLHS in the automaton
AutRHS.

* Contact
   * Adam Rogalewicz <rogalew@fit.vutbr.cz>

* Participation
   * 2014: /=UDB_entl=/, /=FDB_entl=/
   * 2018: /=qf_shid_entl=/, /=qf_shlid_entl=/, /=shid_entl=/


# Songbird

* Contact
   * Ta Quang Trung <taquangtrungvn@gmail.com>
   * Chin Wei Ngan <chinwn@comp.nus.edu.sg>

* Participation
   * 2018: all


#  SPEN

SPEN is an open source solver for checking validity of entailments between formulas
in a fragment of Separation Logic with inductive definitions and linear integer
constraints. The internals are published in

* References
   * Constantin Enea, Ondrej Lengal, Mihaela Sighireanu, and Tomas Vojnar.
   Compositional entailment checking for a fragment of separation logic.
   In Proc. of APLAS’14, volume 8858 of LNCS, pages 314–333. Springer, 2014

   * Constantin Enea, Mihaela Sighireanu, and Zhilin Wu.
   On automated lemma generation for separation logic with inductive definitions.
   In ATVA’15, volume 9364 of LNCS, pages 80–96. Springer, 2015.

* Contact
   * Mihaela Sighireanu <mihaela.sighireanu@gmail.com>

* Participation
   * 2014: /=FDB_entl=/, /=sll0a_entl=/, /=sll0a_sat=/
   * 2018: /=qf_shls_sat=/, /=qf_shls_entl=/, /=qf_shlid_entl=/,
   /=qf_shid_entl=/, /=qf_shid_sat=/
