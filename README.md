# OpenFoam-Open-Channel-Flow-Tutorial
This tutorial describes simulating open channel flow in OpenFoam with environmental application.

## Open channel flow
Open channel flow is a distinct category of fluid flow (Young et al., Granger)
where there is an interface between the water and atmosphere which
is not assumed constant and also called free surface flow.
This flow type includes many applications in environmental,
coastal, hydraulic and ecological engineering such as dams, weirs, spillways, fish passages, boat wakes and hydraulic structures. There is increased use of CFD
in environmental engineering (Liu and Zhang).
Fluent and other commercial packages are available but OpenFoam is 
free and is useful as the details and source can be modified by the user. 

There are several open channel flow tutorial cases that come with OpenFoam including the
damBreak tutorial and
weirOverflow tutorial.

Certain additional parameter is needed in open channel flow.
First, because the interface between water and air is a free surface need to track this over time.
In these tutorials a new variable called alpha.water which denotes the.....
We have 
$ 0 \le alpha.water \le 1.0$.

### Mesh and boundary and initial conditions - Preprocessing
Mesh....blockMeshDict
when creating the mesh for the problem, we need to in blockMeshDict file have the top boundary (wall)
of domain be atmosphere.

Initial Conditions as with any variable to solve for in simulation, we need to set alpha.water as initial condtion in the domain. 
How to do this in openFoam

Boundary conditions
the patch atmosphere

constant directory
need to include g as a file, where the m/sec2... how is this used in the code?

### Solvers for open channel flow
The finite volume method is used in OpenFoam package to solve the governing PDE equations of Navier-Stokes.
To this we add a variable to solve as discussed above
interFoam solver (multiphase) 
volume of fluid (VOF) method

### 


### Environmental engineering applications using OpenFoam (Literature review)
There are several studies that compare OpenFoam and FLOW-3D commercial CFD software in applications.
