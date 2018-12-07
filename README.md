The Separation Logic Competition (SL-COMP) is an initiative to bring together 
researchers and practitioners interested on improving the state of the art of 
automated deduction methods for 
[Separation Logic](http://www0.cs.ucl.ac.uk/staff/p.ohearn/SeparationLogic/Separation_Logic/SL_Home.html).
The competition is run on more than 1K decision problems for different theories 
of Separation Logic. The solvers are compared on each theory on the number
of problems solved and the running time. 
This initiative started at [FLOC 2014](http://vsl2014.at/) and 
it has been afiliated with different events: 
[SMT-COMP 2014](http://smtcomp.sourceforge.net/2014/), 
[FLOC 2018](https://www.floc18.org) workshop
[ADSL 2018](http://adsl.univ-grenoble-alpes.fr/) and 
[TOOLympics 2019](https://tacas.info/toolympics.php).

# NEWS
* January 8, 2019: Deadline for registration of solvers for SL-COMP 2019 at 
     [easychair submission site](https://easychair.org/conferences/?conf=slcomp19)
* December 7, 2018: Call for participation to SL-COMP 2019 at [TOOLympics 2019](https://tacas.info/toolympics.php)
* July 14, 2018: Results of [SL-COMP 2018](https://www.irif.fr/~sighirea/sl-comp/18/index.html) are presented at 
     [ADSL 2018](http://adsl.univ-grenoble-alpes.fr/)

# Specification and rules

The competition compares solvers for decision problems in Separation Logic with respect to effectiveness and running time. 
The competition consists of two phases: a training phase, in which solver developers try their tool on the competition benchmark and may provide feedback to organizers, and an evaluation phase, in which all participating solvers are executed on benchmark problems, and the number of correctly solved instances as well as the runtime is measured.

A decision problem is either a satisfiability or an entailment problem in a fixed fragment of Separation Logic.
The possible answers of a solver are: *sat*, *unsat* and *unknown*. The answer is compared with the known status of the problem specified in the problem's file. The result of the comparison determines the evaluation of the solver on this problem, which is *correct*, *incorrect* or *unsolved*.

The problems are specified using the format described [here](doc/sl-comp-format.pdf) and commented in this [post](https://groups.google.com/forum/?hl=fr#!topic/sl-comp/3j8iaaLvTWs). 
The input format of problems extends the format [SMT-LIB](http://smtlib.cs.uiowa.edu/index.shtml) with SL constructs, and exploit the new features of SMT-LIB like datatypes definition and mutually recursive functions.

Teams may contribute with problems in the input format above. The number of problems submitted by a team in some division is limited. The problems submitted are revised by the organizing committee which may or may not accept it. An accepted problem may be changed when this improves the overall quality of the final set of problems. 

The solvers shall run on the [StarExec](https://starexec.org) platform. Solvers may use a pre-processor to transform the input file format to the solver's format.The time spent on this pre-processor is not included in the evaluation time. The input problems are not scrambled before their submission to he solver.

# Benchmark and divisions

The set of decision problems collected until now are available for browsing and download on the following [GIT repository](https://github.com/sl-comp/SL-COMP18/tree/master/bench).

Each problem is contributed by a team, as specified in the file header. Thanks to all participants that contributed programs, sent patches, and commented on the sets. 

The file header also specifies the status of the problems (*sat*, *unsat*) and, most importantly, the logic fragment used in this problem. A division is defined by its logic fragment. The following division are now present:
* Satisfiability checking:
    * [**qf_shls_sat**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shls_sat): 
        for quantifier free (QF) formulas in the symbolic heaps (SH) fragment using only acyclic singly linked lists
    * [**qf_shid_sat**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shid_sat): 
       for QF formulas in the SH fragment using general inductive definitions (ID)
    * [**qf_shidlia_sat**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shidlia_sat]: 
       for QF formulas in the SH fragment with ID and linear integer constraints (LIA)
    * [**qf_bsl_sat**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_bsl_sat): 
      for QF fragment with boolean combination of SL atoms; 
      the quantified version of this division [bsl_sat](https://github.com/sl-comp/SL-COMP18/tree/master/bench/bsl_sat) 
      has not enough problems to enter in the competition
    * [**qf_bsllia_sat**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_bsllia_sat): 
      for QF fragment with boolean combination of SL atoms and LIA

* Entailment checking:
    * [**qf_shls_entl**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shls_entl): 
      for QF formulas in the SH fragment using only acyclic singly linked lists
    * [**qf_shid_entl**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shid_entl): 
      for QF formulas in the SH fragment with ID
    * [**qf_shlid_entl**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shlid_entl): 
      for QF formulas in the SH fragment with linear ID
    * [**shid_entl**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/shid_entl): 
      for formulas in the SH fragment with ID
    * [**qf_shidlia_entl**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/qf_shidlia_entl): 
      for formulas in the SH fragment with ID and LIA
    * [**shidlia_entl**](https://github.com/sl-comp/SL-COMP18/tree/master/bench/shidlia_entl): 
      for QF formulas in the SH fragment with IS and LIA

# Tools

The GIT repository provides tools for parsing the input format (in C, C++ and Ocaml).
Based on these tools, the organizing committee provides pre-processors of this input to solvers' input format.

The same repository includes a translator of the input format used for SL-COMP 2014 to the new input format.

# Participants

The following solvers have participated to at least one edition of SL-COMP:
* [Asterix](solvers.md#Asterix) 
* [ComSPEN](solvers.md#CSPEN)
* [Cyclist-SL](solvers.md#CYCLIST)
* [CVC4](solvers.md#CVC4) 
* [Harrsh](solvers.md#Harrsh) 
* [S2S](solvers.md#S2S)
* [Sleek](solvers.md#Sleek)
* [Slide](solvers.md#Slide)
* [Songbird](solvers.md#SB)
* [SPEN](solvers.md#SPEN)


# Previous editions
* [SL-COMP 2018](https://www.irif.fr/~sighirea/sl-comp/18/index.html) at [FLOC 2018](https://www.floc18.org)
* [SL-COMP 2014](https://www.irif.fr/~sighirea/sl-comp/14/index.html) at [FLOC 2014](http://vsl2014.at/)

# Papers

* R. Iosif, C. Serban, A. Reynolds, and M. Sighireanu. *Encoding Separation Logic in SMT-LIB v2.5*.
  [PDF](doc/sl-comp-format.pdf)
* M. Sighireanu and D. R. Cok. *Report on SLCOMP 2014*. JSAT 2014, 
  [PDF](https://www.irif.fr/~sighirea/sl-comp/14/slcomp14-report.pdf)


# Mailing list
  Any question related to this competition shall be sent to
  the organisation committee and to the
  [mailing list](https://groups.google.com/forum/sl-comp).
