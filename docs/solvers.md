
This page describes the solvers that have participated to at least one edition of SL-COMP.

# Asterix 

The solver deals with the satisfiability and entailment checking in the
`QF_SHLS` fragment.
For this, it implements a model-based approach.
The procedure relies on SMT solving technology (Z3 solver is used) 
to untangle potential aliasing between program variables.
It has at its core a matching function that checks whether a 
concrete valuation is a model of the input formula and, if so, 
generalizes it to a larger class of models where the formula is also valid.

* Reference
   * J. A. Navarro Perez and A. Rybalchenko. Separation Logic Modulo Theories.
     In Proc. APLAS'13, 2013.

* Contact
   * Juan Navarro Pérez (at the time at University College London, UK, now at Google) 
    <juannavarroperez@gmail.com>

   * Andrey Rybalchenko (at the time at TU Munich, Germany, now at Microsoft Research Cambridge, UK)
     <rybal@microsoft.com>

* Participation
   * 2014: `sll0a_sat` (winner), `sll0a_entl` (winner)
   * 2018: `qf_shls_sat` (winner), `qf_shls_entl` (winner)
   * 2019: `qf_shls_sat` (winner), `qf_shls_entl` (winner)


# ComSPEN

ComSPEN (for Compositional SPEN) is a solver for the symbolic heap
fragment of SL with compositional ID. It also supports linear integer
arithmetics.

* Contact
   * Zhilin Wu <wuzl@ios.ac.cn>
   * Chong Gao <gaochong@ios.ac.cn>

* Reference 
  * Xincai Gu, Taolue Chen, and Zhilin Wu,
    A Complete Decision Procedure for Linearly Compositional Separation
    Logic with Data Constraints.
    In Proc. IJCAR, volume 9706 of LNCS, Springer, 2016.
    
* Participation
   * 2018 (expected but pull out because of an issue on StarExec)
   * 2019: `qf_shidlia_sat`, `qf_shidlia_entl`, `qf_shlid_entl`, `qf_shls_entl`, `qf_shls_sat`
 
 
# Cyclist-SL

Cyclist-SL deals with the entailment checking for the `QF_SLID` fragment.
It is an instantiation of the theorem prover Cyclist for the case of Separation Logic with inductive definitions.
The solver builds derivation trees and uses induction to cut infinite paths in these trees
that satisfy some soundness condition.
For the Separation Logic, Cyclist-SL replaces the rule of weakening used in first-order theorem provers with the frame rule of SL.

* Contact
   * Nikos Gorogiannis <nikos.gorogiannis@gmail.com>

* References
   * J. Brotherston, N. Gorogiannis, and R. L. Petersen. 
   A generic cyclic theorem prover. I
   n Proc. APLAS-10, pages 350-367. Springer, 2012.


* Participation
   * 2014: `UDB_entl` (winner), `UDB_sat`, `sll0a_entl`, `sll0a_sat`, `FDB_entl`
   * 2018: `qf_shid_entl` (second), `qf_shls_entl`, `qf_shlid_entl`, `shid_entl`
   * 2019: `qf_shid_entl`, `qf_shls_entl`, `qf_shlid_entl`, `shid_entl`


# CVC4

CVC4-SL includes a procedure for the boolean combination of
SL atoms without inductive definitions.

* Contact
   * Andrew J. Reynolds <andrew.j.reynolds@gmail.com>

* Reference
  * Andrew Reynolds, Radu Iosif, Cristina Serban, and Tim King.
    A Decision Procedure for Separation Logic in SMT.
    In Proc. ATVA, Springer, 2016.
    
* Participation
   * 2018: `qf_bsl_sat`, `bsl_sat`
   * 2019: `qf_bsl_sat`, `bsl_sat`


# Harrsh

HARRSH is a prover for symbolic heap separation logic with user defined predicates. 
It can prove satisfiability as well as various reachability based properties of symbolic heaps, 
including garbage freedom and acyclicity. HARRSH is based on Heap Automata, 
as introduced in our ESOP 2017 paper below.

* Contact
   * Jens Katelaan <jkatelaan@forsyte.at>

* Reference
  * Jens Katelaan, Christoph Matheja, Thomas Noll, and Florian Zuleger.
    Harrsh: A Tool for Unied Reasoning about Symbolic-Heap Separation Logic.
    In Proc. LPAR-22, Easychair, 2018.
  * Christina Jansen, Jens Katelaan, Christoph Matheja, Thomas Noll, and Florian Zuleger.
    Unified Reasoning About Robustness Properties of Symbolic-Heap Separation Logic.
    In Proc. ESOP, volume 10201 of LNCS, Springer, 2017.
    
* Participation
   * 2018: `qf_shid_sat`, `qf_shls_sat`
   * 2019: `qf_shid_entl`, `sf_shid_sat` (bronze),
              `qf_shidlia_entl`, `qf_shlid_entl` (bronze),
              `qf_shls_entl`, 


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

* Reference:
   * [https://loc.bitbucket.io/s2s/](Web site)
  
* Participation
   * 2018: `qf_shid_entl`, `qf_shid_sat`,
                `qf_shidlia_entl`, `qf_shidlia_sat` (winner), `qf_shlid_entl` (winner), 
                `qf_shls_entl`, `qf_shls_sat`,
                `shid_entl` (second), `shidlia_entl`
   * 2019: winner in `qf_shid_entl`, `qf_shid_sat`,
                `qf_shidlia_entl`, `qf_shidlia_sat`, 
                `qf_shlid_entl`, `shid_entl`, `shidlia_entl`,
           second in `qf_shls_entl`, `qf_shls_sat`.
                
                
# Sleek

Sleek deals with the satisfiability and entailment checking for the `qf_shid` fragment.
It is an (incomplete but) automatic prover, that builds a proof tree for the input problem 
by using the classical inference rules and the frame rule of SL. It also uses a database of lemmas for the inductive definitions in order to discharge the proof obligations on the spatial formulas.
The proof obligations on pure formulas are discharged by external provers like CVC4, Mona, or Z3.

* Contact
   * Benedict Lee <benedictleejh@gmail.com>
   * Chin Wei Ngan <chinwn@comp.nus.edu.sg>

* Reference
  * Wei-Ngan Chin, Cristina David, Huu Hai Nguyen, and Shengchao Qin.
    Automated verification of shape, size and bag properties
               via user-defined predicates in separation logic.
    In Sci. Comput. Program. 77(9), 2012.
    
* Participation
   * 2014: all, winner `UDB_entl`
   * 2018: all, bronze `qf_shid_entl`


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

* Reference
  * Radu Iosif, Adam Rogalewicz, and Tomas Vojnar.
    Deciding Entailments in Inductive Separation Logic with Tree Automata.
    In Proc. ATVA, volume 8837 of LNCS. Springer, 2014.
  
* Participation
   * 2014: `UDB_entl`, `FDB_entl`
   * 2018: `qf_shid_entl`, `qf_shlid_entl`, `shid_entl`


# SLSAT

SLSAT deals with the satisfiability problem for the `qf_slid` fragment.
The decision procedure is based on a fixed point computation of a constraint, 
called the *base* of an inductive predicate definition. 
This constraint is a conjunction of equalities and dis-equalities between 
a set of free variables built also by the fixed point computation from the set of inductive definitions.

* Contact
   * Nikos Gorogiannis <nikos.gorogiannis@gmail.com>

* References
   * J. Brotherston, C. Fuhs, Juan A. Navarro Perez, and N. Gorogiannis. 
   A decision procedure for satisfiability in separation logic with inductive predicates.
   In Proc. LICS, pages 1-10, ACM, 2014.


* Participation
   * 2014: `UDB_sat` (second), `sll0a_sat`
   * 2018: `qf_shid_sat` (winner), `qf_shls_sat`
   * 2019: `qf_shid_sat` (second), `qf_shls_sat`

# Songbird

Songbird targets `shidlia` fragment and its subfragments. It employs mathematical induction
to prove entailments involving user-defined predicates. In addition,
Songbird is also equipped with powerful proof techniques,
which include a mutual induction proof system and
a lemma synthesis framework.

* Contact
   * Ta Quang Trung <taquangtrungvn@gmail.com>
   * Chin Wei Ngan <chinwn@comp.nus.edu.sg>

* References
   * Quang-Trung Ta, Ton Chanh Le, Siau-Cheng Khoo, and Wei-Ngan Chin.
   Automated Lemma Synthesis in Symbolic-heap Separation Logic.
   In Proc. POPL, pages 1-29, ACM, 2017.
   * Quang-Trung Ta, Ton Chanh Le, Siau-Cheng Khoo, and Wei-Ngan Chin.
   Automated Mutual Explicit Induction Proof in Separation Logic.
   In Proc. FM, volume 9995 of LNCS, pages 659-676, Springer, 2016.
   
* Participation
   * 2018: ALL, winner in `qf_shid_entl`, `qf_shidlia_entl`, `shid_entl`, `shidlia_entl`,
           second in `qf_shidlia_sat`
   * 2019: ALL


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
   * 2014: `FDB_entl` (winner), `sll0a_entl` (bronze), `sll0a_sat` (bronze)
   * 2018: `qf_shls_sat`, `qf_shls_entl`, `qf_shlid_entl`,
   `qf_shid_entl`, `qf_shid_sat`
