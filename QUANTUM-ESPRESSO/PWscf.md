#PWscf
####It can do:

* ground-state energy and one-electron (Kohn-Sham) orbitals, atomic forces, stresses;
* structural optimization, also with variable cell;
* molecular dynamics on the Born-Oppenheimer surface, also with variable cell;
* macroscopic polarization and ﬁnite electric ﬁelds via the modern theory of polarization (Berry Phases);
* modern theory of orbital magnetization;
* free-energy  surface  calculation  at  ﬁxed cell  through  meta-dynamics,  if  patched  with PLUMED.

####Input data:

**&CONTROL** 
general variables controlling the run

**&SYSTEM**
structural  information on the system under investigation

**&ELECTRONS**
 electronic variables: self-consistency, smearing

**&IONS** (*optional*)
 ionic variables: relaxation, dynamics

**&CELL** (*optional*)
variable-cell optimization or dynamics

aa|aa|aa
:--|:--|--:
aaaaa|bb|bbbbb
