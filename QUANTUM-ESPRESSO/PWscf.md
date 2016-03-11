#PWscf
####It can do:

* ground-state energy and one-electron (Kohn-Sham) orbitals, atomic forces, stresses;
* structural optimization, also with variable cell;
* molecular dynamics on the Born-Oppenheimer surface, also with variable cell;
* macroscopic polarization and ﬁnite electric ﬁelds via the modern theory of polarization (Berry Phases);
* modern theory of orbital magnetization;
* free-energy  surface  calculation  at  ﬁxed cell  through  meta-dynamics,  if  patched  with PLUMED.
 
####Tools in PW/tools:

* **dist.x**  reads input data for **PWscf**, calculates distances and angles between atoms in a cell, taking into account periodicity
* **ev.x** fits energy-vs-volume data to an equation of state
* **kpoints.x** produces lists of k-points
* **pwi2xsf.sh, pwo2xsf.sh** process respectively input and output files for **pw.x** and produce and XSF-formatted file suitable for plotting with XCrySDen
* **bs.awk, mv.awk** process the output of pw.x
* **cif2qe.sh** converting from CIF to a format suitable for QUANTUM ESPRESSO

***

####Input data:

#####NAMELISTS:

* **&CONTROL** general variables controlling the run
* **&SYSTEM** structural  information on the system under investigation
* **&ELECTRONS** electronic variables: self-consistency, smearing
* **&IONS** ( *optional* ) ionic variables: relaxation, dynamics
* **&CELL** ( *optional* ) variable-cell optimization or dynamics

#####AND CARDS:

* **ATOMIC_SPECIES**
* **ATOMIC_POSITIONS**
* **K_POINTS**
* **CELL_PARAMETERS** ( *optional* )
* **OCCUPATIONS** ( *optional* )

####All the variables have default values **EXCEPT**:

* **ibrav** ( *integer* ) : Bravais_lattice index
* **celldm** ( *real, dimension 6* ) : crystallographic constants
* **nat** ( *integer* ) : number of atoms in the unit cell
* **ntyp** ( *integer* ) : number of types of atoms in the unit cell
* **ecutwfc** ( *real* ) : kinetic energy cutoff (Ry) for wavefunctions.

    Power by makedown
