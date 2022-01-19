---
layout: page
title: About
---
 Octo-Tiger is particularly suited to modelling interacting binary star systems. Its self consistent field (SCF) code enables the production of initial conditions for
 binaries with barotropic equations of state. The user may set the masses of the components, their Roche lobe filling factors, their separation, and their structural equations of state (which may
 be polytropic, bi-polytropic, or white dwarf). It is possible to produce detached, semi-detached, and contact binaries. These options allows Octo-Tiger to produce approximate initial conditions 
 many binary systems including double white dwarves, main sequence binaries, as well as contact binaries such as V1309 Sco. 

 With initial conditions from the SCF, Octo-Tiger's hydro and gravity modules are 
 used to evolve the system in time. The system is placed in a mesh corotating with the initial orbital frequency of the binary, reducing numerical diffusion. The hydro solver uses a fully multi-dimensional 
 finite volume method. Rather than reconstructing the evolved quantities on cell faces alone, the third order PPM reconstruction is applied to produced values at the centers of cell faces, the centers of cell edges,
 and cell vertices. The numerical flux is then computed by quadrature from the 9 available reconstruction points on each face. This fully multi-dimensional reconstruction helps better reproduce
 roughly spherical equilibrium structures such as stars. We also apply the dual energy formalism to provide better accuracy when kinetic energy
 far exceeds internal energy. The system is advanced in time using the method of lines with a third order TVD Runge Kutta solver. 

  The gravity solver is a fast multipole method (FMM)
 solver. Like most FMM's, Octo-Tiger's FMM conserves linear momentum to machine precision. We have modified the FMM so that it also conserves angular momentum to machine precision. 
 Octo-Tiger computes both the graviational potential as well as the time derivative of the gravitational potential at every RK sub-step. The availability of the time derivative of the potential
 enables the hydro energy equation to be evolved in a way that conserves total energy (potential + kinetic + internal) to machine precision, and the conservation of angular momentum by the gravity solver
 enables this feature to be extended to the rotating frame. Without conservation of total energy, stellar structures in equilibrium tend to "evaporate" over time due to numerical diffusion at their boundaries
 and in their cores.

 Octo-Tiger also contains a radiation module which is not yet fully tested. It evolves the transport part of the radiation equation using explicit sub-stepping and the hydro coupling terms with an
 implicit method. It uses a two moment method, evolving both the radiation energy and the radiation momentum. The radiation momentum equation is closed using an approximation for the Eddington tensor 
 computed from the radiation momentum and energy for a given cell.
 
 Octo-Tiger provided both visualization output as well as checkpointing capabilities through the use of the SILO format. These files are viewable with the VisIt software. There are also
 on the fly analysis tools which compute quantities such as the masses of each component, their spins and their energies, as well as quantities related to the binary as a whole such as binary separation orbital
 frequency. These files are appended every time refinement is checked for, enabling monitoring of the simulation as it progresses.
 
