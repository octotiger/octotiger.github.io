---
layout: page
title: Applications
---

1. Simulating 3D Merger Events to 1D Stellar Evolution

R Coronae Borealis (RCB) stars are rare hydrogen-deficient carbon-rich variable supergiants thought to be the result of dynamically unstable white dwarf mergers. To model RCB stars through all the relevant timescales, a merger simulation of mass ratio 0.6 carried out by Octo-Tiger was mapped into MESA, a 1D stellar evolution code. Since the surface abundances of RCB stars are consistent with partial He burning, it is important to have a hot shell above the carbon-oxygen (CO) core that has a sufficient temperature to ignite helium (He) burning. 
Octo-tiger was initialized with a 0.53 solar mass CO WD and a 0.32 solar mass He WD. A zero-temperature WD (ZTWD) and ideal gas EOS was used. , which assumes a zero-temperature electron gas with a mean molecular weight per free electron of 2 atomic units. The mean molecular weight for ions and electrons used in the ideal gas EOS is calculated for fully ionized He for the secondary (4/3 atomic units) and an equal mixture of fully ionized C and O by mass for the primary (1.75 atomic units). The initial orbital period of the binary is 149 s, and the initial grid is 24,000 subgrids with up to seven levels of refinement based o density. Because Octo-tiger does not handle gravitational radiation or magnetic fields, angular momentum is removed from the system at a user-defined rate. For this system, the dynamically unstable merger event initiates after about an hour. After 3.3 hr of evolution in Octo-tiger, we spherically average the grid to be mapped into MESA. a hot shell is clearly visible and has a peak temperature of about 285 MK still high enough to initiate He burning.
The post-merger object was spherically averaged many orbits after the merger. After relaxation and evolved in MESA. The advantage of evolving the post merger in a stellar evolution code is that both the mixing of the elements and the nucleosynthesis, as well as other aspects like mass loss and rotation are simulated simultaneously. The obtained models match observations or previous studies in most surface abundances, isotopic ratios, early evolution, and lifetimes. We also observe similar mixing behavior to previous modeling attempts that result in the partial He-burning products visible on the surface in observations.  
In addition, such studies allow the exploration of other effects like convection overshooting, or sub-solar metallicities, which are difficult to explore in a dynamical merger simulation. Munson et al. 2021 found that at the timescale of 1000 years the merger will have a luminosity and effective temperature that are in range of the observed luminosities and effective temperatures of RCB stars. The star spends approximately 10^5 years at this phase. They report the surface abundance right when the star reaches minimal effective temperature and find a general agreement in most of the key elements. They find that overshooting mixes more Helium and therefore enhances the production of O-18. However, at some point, a further overshooting brings O-16 from down the core, and the O-16 to O-18 ratio substantially increases.

![](munson2021.png)
 *A merger of a 0.5 solar mass carbon-oxygen white dwarf and a 0.3 solar mass helium white dwarf. Pseudocolor plot of the density in a slice of the equatorial plane after 3.3 hours of evolution (2.3 hours after merger)* 

[Munson et. al 2021: R Coronae Borealis Star Evolution: Simulating 3D Merger Events to 1D Stellar Evolution Including Large-scale Nucleosynthesis](https://ui.adsabs.harvard.edu/abs/2021ApJ...911..103M/abstract)

2. Simulating a Red Super Giant Star Merging with a Main-Sequence Star
3. Reproducing polygonal resonances at high mass transfer rates
