## Tutorials on Julia for ChEs and BioChEs

### Introduction

This repository contains tutorials for the free and open-source [Julia](https://julialang.org/) programming language that are especially tailored for chemical and biochemical engineers (ChEs and BioChEs). Julia is a relatively new programming language that provides an unequaled combination of programming ease and computational speed. In addition, the tutorials shown here emphasize using the Julia software package [ModelingToolkit.jl](https://docs.sciml.ai/ModelingToolkit/stable/) in order to combine symbolic and numeric approaches for solving problems of interest to ChEs and BioChEs. ModelingToolkit.jl provides an efficient user interface for Julia packages relevant to symbolic-numeric computing such as [Symbolics.jl](https://docs.sciml.ai/Symbolics/stable/), which is a fast computer algebra system, and [DifferentialEquations.jl](https://docs.sciml.ai/DiffEqDocs/stable/), which is a highly developed package for numerical solutions of differential equations. Combining symbolic and numeric approaches in this way enables both more effective solution methods and more efficient compiled numerical code for existing methods. In addition, a pure Julia, single-language approach helps to coordinate the various parts of the overall computational method. ModelingToolkit.jl can also perform either causal or acausal simulations, in contrast to [Modelica](https://modelica.org/), which is strictly acausual, and [Simulink](https://www.mathworks.com/products/simulink.html), which is strictly causal. 

Although many tutorials exist for the Julia programming language, none have the focus of this tutorial, and many are somewhat short on using effective pedagogical methods to make learning easy (or at least easier!) for the neophyte. The tutorials here seek to address these needs.

### Julia packages built on ModelingToolkit.jl

There are several software libraries in the Julia ecosystem that are built on top of ModelingToolkit.jl to take advantage of its features. Examples include the following:

| Software | Purpose| License Type|
|  ---  |  ---  |  ---  |
|[Catalyst.jl](https://docs.sciml.ai/Catalyst/stable/)| Simulation of chemical and biochemical reaction networks| Free and open source |
|[DataDrivenDiffEq.jl](https://docs.sciml.ai/DataDrivenDiffEq/stable/)| Automatically find the system of governing symbolic equations that corresponds to a dataset| Free and open source |
|[MethodOfLines.jl](https://docs.sciml.ai/MethodOfLines/stable/)| Solving PDEs using the Method of Lines| Free and open source |
|[NeuralPDE.jl](https://docs.sciml.ai/NeuralPDE/stable/)| Solving PDEs using Physics Informed Neural Networks (PINNs)| Free and open source |
|[ProcessSimulator.jl](https://github.com/SciML/ProcessSimulator.jl)| Simulation of chemical processes (such as vapor-liquid equilibrium flash etc.)| Free and open source |
|[NumCME.jl](https://voduchuy.github.io/NumCME.jl/dev/)| Chemical Master Equation approach for simulating biochemical reaction networks| Free and open source |
|[ModelingToolkitNeuralNets.jl](https://docs.sciml.ai/ModelingToolkitNeuralNets/stable/)| Embed a neural network inside a ModelingToolkit equation system| Free and open source |
|[MomentClosure.jl](https://sciml.github.io/MomentClosure.jl/dev/)| Solve differential equations in term of the moments of the time functions (e.g., mean, variance, etc.) as opposed to the time functions themselves| Free and open source|
|[Neuroblox](https://www.neuroblox.ai/)| Computational neuroscience and psychiatry| Free for non-commercial use, a monthly fee otherwise |
|[PumasAI](https://pumas.ai/)| Pharmacometrics | Free for non-commercial use, a monthly fee otherwise |
|[Dyad](https://juliahub.com/products/dyad)| A declarative, physical modeling language that compiles into ModelingToolkit.jl code and permits AI-assisted industrial modeling| Free for non-commercial use, a monthly fee otherwise |

In addition to general applications of ModelingToolkit.jl, this tutotial also includes the specific use of Catalyst.jl and DataDrivenDiffEq.jl from the above table since symbolic-numeric computing is central to the operation of these two packages. More generally, since all of the above software packages have ModelingToolkit.jl as their foundation, familiarity with ModelingToolkit.jl greatly facilitates their use.  

### References

1.  S. Gowda, Symbolic-Numeric Programming in Scientific Computing, PhD thesis, MIT, 2024.

### Links to tutorial sections:

Part 1: Setup

&nbsp;&nbsp;&nbsp;&nbsp;[Installing and using Julia](https://github.com/dougfrey/Julia_tutorials_for_ChEs/blob/main/Part%201%3A%20Setup/Installing_and_Using_Julia.md)
  
&nbsp;&nbsp;&nbsp;&nbsp;[Installing and using Jupyter](https://github.com/dougfrey/Julia_tutorials_for_ChEs/blob/main/Part%201%3A%20Setup/Installing_and_Using_Jupyter_Notebooks.md)

Part 2: Background Information

&nbsp;&nbsp;&nbsp;&nbsp;Description of ModelingToolkit.jl

&nbsp;&nbsp;&nbsp;&nbsp;Summary of Concepts Used

Part 3: Solving Nonlinear Algebraic Equations

&nbsp;&nbsp;&nbsp;&nbsp;Solvers Used

&nbsp;&nbsp;&nbsp;&nbsp;Problem to be Solved -- Ion-Exchange Equilibrium
