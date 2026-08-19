## Tutorials on Julia for ChEs and BioChEs

### Introduction

This repository contains tutorials for the free and open-source [Julia](https://julialang.org/) programming language that are especially tailored for chemical and biochemical engineers (ChEs and BioChEs). Julia is a relatively new programming language that provides an unequaled combination of programming ease and computational speed. The tutorials shown here are also geared toward persons who already know the Matlab programming language since Julia and Matlab have many similarities. 

The tutorials shown here emphasize using the Julia software package [ModelingToolkit.jl](https://docs.sciml.ai/ModelingToolkit/stable/) (MTK) in order to combine symbolic and numeric approaches for solving problems (see Refs. 1 and 2).  MTK provides an efficient user interface for Julia packages relevant to symbolic-numeric computing such as [Symbolics.jl](https://docs.sciml.ai/Symbolics/stable/), which is a fast computer algebra system, and [DifferentialEquations.jl](https://docs.sciml.ai/DiffEqDocs/stable/), which is a highly developed package for numerical solutions of differential equations. Combining symbolic and numeric approaches so that they co-exist and inform each other enables more effective solution methods and more efficient compiled numerical code. Furthermore, due to MTK's many automated features, this modeling approach can be accomplished by someone with modest mathematical and numerical modeling skills. In addition, a pure Julia, single-language approach helps to coordinate the various parts of the overall computational method. MTK can also be used for either causal or acausal modeling, in contrast to [Modelica](https://modelica.org/), which is strictly acausual, and [Simulink](https://www.mathworks.com/products/simulink.html), which is strictly causal. 

In the typical university curricula for undergraduate and graduate ChE and BioChE, computational problems are formulated so that they are "toy" in nature and essentially any computational platform will suffice for their solution. In contrast, this tutorial is aimed at realistic, real-world, and large-scale applications where computational efficiency is important. This tutorial is especially aimed at the common situation where someone is using a typical laptop or desktop personal computer and needs to achieve the performance of a high-end workstation.       

Although many tutorials exist for the Julia programming language, none have the focus of this tutorial, and many are somewhat short on using effective pedagogical methods to make learning easy (or at least easier!) for the neophyte. The tutorials here seek to address these needs.  So, fasten your seatbelts, hold on to your hats, and join us for a wild ride in the Julia language ecosystem.

### Julia packages built upon ModelingToolkit.jl (MTK)

There are several software libraries in the Julia ecosystem that are built upon MTK to take advantage of its features. Selected examples, in alphabetical order, include the following: 

| Software | Purpose| License Type|
|  ---  |  ---  |  ---  |
|[Aerosol.jl](https://aerosol.earthsci.dev/stable/)| Modeling of atmospheric aerosols| Free and open source |
|[Catalyst.jl](https://docs.sciml.ai/Catalyst/stable/)| Modeling of chemical and biochemical reaction networks (see Ref. 3)| Free and open source |
|[DataDrivenDiffEq.jl](https://docs.sciml.ai/DataDrivenDiffEq/stable/)| Automatically find the system of governing symbolic equations that corresponds to a dataset| Free and open source |
|[Dyad](https://www.hpcwire.com/off-the-wire/juliahub-launches-dyad-for-ai-driven-engineering-and-system-modeling/)| A declarative, physical modeling language that compiles into a ModelingToolkit.jl representation and permits AI-assisted industrial modeling| Free for non-commercial use, a monthly fee otherwise |
|[MethodOfLines.jl](https://docs.sciml.ai/MethodOfLines/stable/)| Solving PDEs using the Method of Lines| Free and open source |
|[ModelingToolkitNeuralNets.jl](https://docs.sciml.ai/ModelingToolkitNeuralNets/stable/)| Embed a neural network inside a ModelingToolkit equation system| Free and open source |
|[MomentClosure.jl](https://sciml.github.io/MomentClosure.jl/dev/)| Solve differential equations in term of the moments of the time functions (e.g., mean, variance, etc.) as opposed to the time functions themselves| Free and open source|
|[Neuroblox](https://www.neuroblox.ai/)| Computational neuroscience and psychiatry (see Ref. 4)| Free for non-commercial use, a monthly fee otherwise |
|[NeuralPDE.jl](https://docs.sciml.ai/NeuralPDE/stable/)| Solving PDEs using Physics Informed Neural Networks (PINNs)| Free and open source |
|[NumCME.jl](https://voduchuy.github.io/NumCME.jl/dev/)| Chemical Master Equation approach for simulating biochemical reaction networks| Free and open source |
|[ProcessSimulator.jl](https://github.com/SciML/ProcessSimulator.jl/blob/sigle-phase-approach/README.md)| Simulation of chemical processes (such as single-stage equilibrium flash etc.) (see Ref. 5)| Free and open source |
|[PumasAI](https://pumas.ai/)| Pharmacometrics with machine learning| Free for non-commercial use, a monthly fee otherwise |
|[Thetis.jl](https://datinfo.gitlab.io/Thetis.jl/stable/)| Modeling of wastewater treatment processes such as activated sludge processes| Free and open source|
|[WildlandFire.jl](https://fire.earthsci.dev/dev/)| Modeling wild fires| Free and open source|

In addition to general applications of MTK, this tutotial also includes the specific use of Catalyst.jl and DataDrivenDiffEq.jl from the above table since symbolic-numeric computing is central to the operation of these two packages. This tutorial also briefly includes the use of ProcessSimulator.jl.  Although this package is in an early stage of development, it nevertheless shows the future of chemical process modeling since it is free and open source, fully differentiable, highly performant, easily customizable, and able to bridge symbolic and numeric representations to enhance the modeling. More generally, since all of the above software packages have MTK as their foundation, familiarity with MTK greatly facilitates their use.  

### References

1.  Y. Ma et al., [ModelingToolkit: A composable graph transformation system for equation-based modeling](https://arxiv.org/abs/2103.05244), ArXiv:2103.05244v3, 2022.

2.  S. Gowda, [Symbolic-numeric programming in scientific computing](https://dspace.mit.edu/entities/publication/185c3adf-eb94-4acf-9e77-f66cb773b71b), PhD thesis, MIT, 2024.

3.  T.E. Loman et al., [Catalyst: Fast and flexible modeling of reaction networks](https://pmc.ncbi.nlm.nih.gov/articles/PMC10584191/), PLOS Computational Biology, e1011530, 2023.

4.  D. Hofmann et al., [Increasing spectral dynamic causal modeling (sDCM) flexibility and speed by leveraging ModelingToolkit and automated differentiation](https://pmc.ncbi.nlm.nih.gov/articles/PMC12330849/), Imaging Neuroscience, vol. 3, 2025

5.  V. V. Santana et al., [ProcessSimulator.jl: A symbolic-numeric open-source framework for process simulation in Julia language](https://psecommunity.org/LAPSE:2026.0385), Systems and Control Transactions, vol. 5, 1439-1444, 2026. 

### Links to tutorial sections:

Part 1: Setup

&nbsp;&nbsp;&nbsp;&nbsp;[Installing and using Julia](https://github.com/dougfrey/Julia_tutorials_for_ChEs/blob/main/Part%201%3A%20Setup/Installing_and_Using_Julia.md)
  
&nbsp;&nbsp;&nbsp;&nbsp;[Installing and using Jupyter](https://github.com/dougfrey/Julia_tutorials_for_ChEs/blob/main/Part%201%3A%20Setup/Installing_and_Using_Jupyter_Notebooks.md)

Part 2: Background Information

&nbsp;&nbsp;&nbsp;&nbsp;[Description of ModelingToolkit.jl (MTK)](https://github.com/dougfrey/Tutorials_on_Julia_for_ChEs_and_BioChEs/blob/main/Part%202%3A%20Background%20Information/Description_of_ModelingToolkit.md)

&nbsp;&nbsp;&nbsp;&nbsp;[Summary of Programming Concepts Used](https://github.com/dougfrey/Tutorials_on_Julia_for_ChEs_and_BioChEs/blob/main/Part%202%3A%20Background%20Information/Summary_of_Programming_Concepts_Used.md)

&nbsp;&nbsp;&nbsp;&nbsp;Working with Vectors

&nbsp;&nbsp;&nbsp;&nbsp;Macros, Types and Fields

Part 3: Solving Nonlinear Algebraic Equations

&nbsp;&nbsp;&nbsp;&nbsp;[Solvers Used](https://github.com/dougfrey/Tutorials_on_Julia_for_ChEs_and_BioChEs/blob/main/Part%203%3A%20Solving%20Nonlinear%20Algebraic%20Equations/1_Solvers_Used.md)

&nbsp;&nbsp;&nbsp;&nbsp;[Problem to be Solved: Ion-Exchange Equilibrium](https://github.com/dougfrey/Tutorials_on_Julia_for_ChEs_and_BioChEs/blob/main/Part%203%3A%20Solving%20Nonlinear%20Algebraic%20Equations/2_Problem_to_be_Solved--Ion_Exchange_Equilibrium.md)

&nbsp;&nbsp;&nbsp;&nbsp;Basic Approach

&nbsp;&nbsp;&nbsp;&nbsp;Working with Indices

&nbsp;&nbsp;&nbsp;&nbsp;Highly Nonlinear Systems

&nbsp;&nbsp;&nbsp;&nbsp;Large Systems
