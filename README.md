## Tutorials on Julia for ChEs and BioChEs

### Introduction

As described in more detail in Ref. 1 given below, all mechanistic models of physical processes start as a symbolic set of equations, possibly produced by pencil and paper or, in more recent times, by symbolic software such as Mathematica or Maple. Then, in a subsequent step, this symbolic representation is transformed (often manually) into numerical code and finally compiled into performant machine code using, e.g., C. However, there is much to be gained by combining these steps into the new paradigm of symbolic-numeric programming where the symbolic and numeric representations of a model co-exist in a single, active environment so they can co-evolve synergistically when needed. This strategy yields new approaches for creating and using models and more efficient final compiled code.        

This repository contains tutorials that are especially tailored for chemical, biochemical and environmental engineers (ChEs, BioChEs, and EnvEs). This repository also introduces the tutorial user to the above modeling approach using the free and open-source [Julia](https://julialang.org/) programming language. Julia is a relatively new programming language that provides an unequaled combination of programming ease and computational speed. Julia is also highly suitable for symbolic-numeric programming due to its reliance on multiple dispatch as a foundational element. The tutorials shown here are also geared toward persons who already know the Matlab programming language since the syntax for Julia and Matlab have many similarities. 

The tutorials shown here emphasize using the Julia software package [ModelingToolkit.jl](https://docs.sciml.ai/ModelingToolkit/stable/) (MTK) in order to combine symbolic and numeric approaches for solving problems (see Ref. 2). MTK provides an efficient user interface that coordinates packages relevant to symbolic-numeric computing such as [Symbolics.jl](https://docs.sciml.ai/Symbolics/stable/), which is a fast computer algebra system, and [DifferentialEquations.jl](https://docs.sciml.ai/DiffEqDocs/stable/), which is a state-of-the-art package for numerical solutions of differential equations. As mentioned above, combining symbolic and numeric approaches enables more effective solution methods and more efficient compiled numerical code. For example, as will be demonstrated later, this approach makes it simple to efficiently generate a symbolic Jacobian when solving nonlinear algebraic equations even when the system is very large. In many cases this yields the fastest numerical code for this type of problem. Furthermore, due to MTK's many automated features, this modeling approach can be accomplished by someone with modest mathematical and numerical modeling skills. 

It is also worth noting that a pure Julia, single-language approach helps to coordinate the various parts of the overall computational method. One reason for this is that Julia and MTK feature both high a level of abstraction and usability and a high level of computational performance so that, for a modeling project that requires teamwork between mathmeticans, engineers, and computer scientists, these individuals are not longer siloed using different tools. Instead, everyone can use the Julia/MTK ecosystem to enhance the communication and collaboration among team members. Finally MTK can also be used for either causal or acausal modeling, in contrast to [Modelica](https://modelica.org/), which is strictly acausual, and [Simulink](https://www.mathworks.com/products/simulink.html), which is strictly causal.   

In the typical university curricula for undergraduate and graduate students, computational problems are formulated so that they are "toy" in nature and essentially any computational platform will suffice for their solution. In contrast, this tutorial is aimed at realistic, real-world, and large-scale applications where computational efficiency is important. This tutorial is especially aimed at the common situation where someone is using a typical laptop or desktop personal computer and needs to achieve the performance of a high-end workstation.       

Although many tutorials exist for the Julia programming language, none have the focus of this tutorial, and many are somewhat short on using effective pedagogical methods to make learning easy (or at least easier!) for the neophyte. The tutorials here seek to address these needs.  So, fasten your seatbelts, hold on to your hats, and join us for an exciting ride in the Julia language ecosystem.

### Julia packages built upon ModelingToolkit.jl (MTK)

There are many software libraries in the Julia ecosystem that are built upon MTK to take advantage of the approaches described above. Selected examples, in alphabetical order, include the following: 

| Software | Purpose| License Type|
|  ---  |  ---  |  ---  |
|[Aerosol.jl](https://aerosol.earthsci.dev/stable/)| Modeling of atmospheric aerosols| Free and open source |
|[Catalyst.jl](https://docs.sciml.ai/Catalyst/stable/)| Modeling of chemical and biochemical reaction networks (see Ref. 3)| Free and open source |
|[DataDrivenDiffEq.jl](https://docs.sciml.ai/DataDrivenDiffEq/stable/)| Automatically find the system of governing symbolic equations that corresponds to a dataset| Free and open source |
|[Dyad](https://www.hpcwire.com/off-the-wire/juliahub-launches-dyad-for-ai-driven-engineering-and-system-modeling/)| A declarative, physical modeling language that compiles into a ModelingToolkit.jl representation and permits AI-assisted industrial modeling| Free for non-commercial use, a monthly fee otherwise |
|[MethodOfLines.jl](https://docs.sciml.ai/MethodOfLines/stable/)| Solving PDEs using the Method of Lines| Free and open source |
|[ModelingToolkitNeuralNets.jl](https://docs.sciml.ai/ModelingToolkitNeuralNets/stable/)| Embed a neural network inside a ModelingToolkit equation system| Free and open source |
|[MomentClosure.jl](https://sciml.github.io/MomentClosure.jl/dev/)| Solve differential equations in term of the moments of the time functions (e.g., mean, variance, etc.) as opposed to the time functions themselves (see Ref. 4)| Free and open source|
|[NeuralPDE.jl](https://docs.sciml.ai/NeuralPDE/stable/)| Solving PDEs using Physics Informed Neural Networks (PINNs)| Free and open source |
|[Neuroblox](https://www.neuroblox.ai/)| Computational neuroscience and psychiatry (see Ref. 5)| Free for non-commercial use, a monthly fee otherwise |
|[NumCME.jl](https://voduchuy.github.io/NumCME.jl/dev/)| Chemical Master Equation approach for simulating biochemical reaction networks| Free and open source |
|[ProcessSimulator.jl](https://github.com/SciML/ProcessSimulator.jl/blob/sigle-phase-approach/README.md)| Simulation of chemical processes (such as single-stage equilibrium flash etc.) (see Ref. 6)| Free and open source |
|[PumasAI](https://pumas.ai/)| Pharmacometrics with machine learning| Free for non-commercial use, a monthly fee otherwise |
|[SymBoltz.jl](https://hersle.github.io/SymBoltz.jl/stable/)| Solving the Einstein-Boltzmann equation in cosmology (see Ref. 7)| Free and open source| 
|[Thetis.jl](https://datinfo.gitlab.io/Thetis.jl/stable/)| Modeling of wastewater treatment processes such as activated sludge processes| Free and open source|
|[WildlandFire.jl](https://fire.earthsci.dev/dev/)| Modeling wild fires| Free and open source|

In addition to general applications of MTK, this tutotial also includes the specific use of Catalyst.jl and DataDrivenDiffEq.jl from the above table since symbolic-numeric computing is central to the operation of these two packages. This tutorial also briefly includes the use ProcessSimulator.jl and Thetis.jl. Although these two package are in a relatively early stage of development, they nevertheless show the future of chemical and wastewater process modeling since they are free and open source, fully differentiable, highly performant, easily customizable, and able to bridge symbolic and numeric representations to enhance the modeling. More generally, since all of the above software packages have MTK as their foundation, familiarity with MTK greatly facilitates their use.  

### References

1.  S. Gowda, [Symbolic-numeric programming in scientific computing](https://dspace.mit.edu/entities/publication/185c3adf-eb94-4acf-9e77-f66cb773b71b), PhD thesis, MIT, 2024.

2.  Y. Ma et al., [ModelingToolkit: A composable graph transformation system for equation-based modeling](https://arxiv.org/abs/2103.05244), ArXiv:2103.05244v3, 2022.

3.  T.E. Loman et al., [Catalyst: Fast and flexible modeling of reaction networks](https://pmc.ncbi.nlm.nih.gov/articles/PMC10584191/), PLOS Computational Biology, e1011530, 2023.

4.  A. Sukys et al., [MomentClosure.jl: Automated moment closure approximations in Julia](https://academic.oup.com/bioinformatics/article/38/1/289/6309452) Bioinformatics, vol. 38, 289-290, 2022.

5.  D. Hofmann et al., [Increasing spectral dynamic causal modeling (sDCM) flexibility and speed by leveraging ModelingToolkit and automated differentiation](https://pmc.ncbi.nlm.nih.gov/articles/PMC12330849/), Imaging Neuroscience, vol. 3, 2025

6.  V. V. Santana et al., [ProcessSimulator.jl: A symbolic-numeric open-source framework for process simulation in Julia language](https://psecommunity.org/LAPSE:2026.0385), Systems and Control Transactions, vol. 5, 1439-1444, 2026.

7.  H. Sletmoen, [SymBoltz.jl: A symbolic-numeric, approximation free, and differentiable linear Einstein-Boltzmann solver](https://www.aanda.org/articles/aa/full_html/2026/03/aa57450-25/aa57450-25.html), Astronomy and Astrophysics, vol. 707, A128, 2026. 

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

Part 4: Optimization

Part 5: ODEs and DAEs

Part 6: Catalyst.jl

Part 7: DataDrivenDiffEq.jl
