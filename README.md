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
- Dec 6, 2018: Call for participation to SL-COMP 2019 at [TOOLympics 2019](https://tacas.info/toolympics.php)
- July 14, 2018: Results of [SL-COMP 2018](https://www.irif.fr/~sighirea/sl-comp/18/index.html) are presented at [ADSL 2018](http://adsl.univ-grenoble-alpes.fr/)

# Competition specification and rules

The competition compares solvers for decision problems in Separation Logic with respect to effectiveness and running time. 
The competition consists of two phases: a training phase, in which solver developers try their tool on the competition benchmark and may provide feedback to organizers, and an evaluation phase, in which all participating solvers are executed on benchmark problems, and the number of correctly solved instances as well as the runtime is measured.

A decision problem is either a satisfiability or an entailment problem in a fixed fragment of Separation Logic.
The possible answers of a solver are: *sat*, *unsat* and *unknown*. The answer is compared with the known status of the problem specified in the problem's file. The result of the comparison determines the evaluation of the solver on this problem, which is *correct*, *incorrect* or *unsolved*.

 The input problems are specified using the format described [here](doc/sl-comp-format.pdf) and commented in this [post](https://groups.google.com/forum/?hl=fr#!topic/sl-comp/3j8iaaLvTWs).

The solvers shall run on the [StarExec](https://starexec.org) platform. Solvers may use a pre-processor to transform the input file format to the solver's format. The input problems are not scrambled. 

# Benchmarks and divisions

# Tools

# Participants

# Previous editions
- [SL-COMP 2018](https://www.irif.fr/~sighirea/sl-comp/18/index.html) at [FLOC 2018](https://www.floc18.org)
- [SL-COMP 2014](https://www.irif.fr/~sighirea/sl-comp/14/index.html) at [FLOC 2014](http://vsl2014.at/)

# Papers

# Mailing list
  Any question related to this competition shall be sent to
  the organisation committee and to the
  [mailing list](https://groups.google.com/forum/sl-comp).
