# Summary of Rajib Roys' selected Github Repositories

## Symmetry Preserving Velocity Projection, Pressure Correction Foam ([spvppcFoam](https://github.com/rroyCFD/spvppcFoam))

### Description
Transient solver for incompressible, turbulent flow, using the Symmetry Preserving, Velocity Projection, Pressure Correction (SPVPPC) algorithm. Implemented using the following the publications:

    Trias, F. X., Lehmkuhl, O., Oliva, A., Pérez-Segarra, C. D., & Verstappen, R. W. C. P. (2014)
    Symmetry-preserving discretization of Navier–Stokes equations on collocated unstructured grids
    Journal of Computational Physics, 258, 246–267
    https://doi.org/10.1016/j.jcp.2013.10.031

and

    Verstappen, R. (2008)
    On restraining the production of small scales of motion in a turbulent channel flow
    Computers & Fluids, 37(7), 887–897
    https://doi.org/10.1016/J.COMPFLUID.2007.01.013


#### Advantages: 

- Compared to the traditional iterative algorithms (e.g. SIMPLE), SPVPPC is a computationally inexpensive modified projection method
- Can eliminate numerical dissipation (with careful selection of discretization schemes and differential operators) which helps to achieve kinetic energy conservation
- Allow regularization of the non-linear convection term to minimize the generation of unphysical, high-frequency scales that leads to excessive dissipation
- Regularization also aids to reduce dissipation induced by the Rhie-Chow correction in collocated finite volume based formulation

*** Requires the __LES regularization class__ to perform the non-linear convective term regularization.
