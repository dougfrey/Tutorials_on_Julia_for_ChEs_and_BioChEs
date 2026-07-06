##  Summary of Concepts and Sytax Used

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This tutorial is intended for those who already have some programming experience (e.g., with MATLAB) and who want to learn simultaneously the basics of Julia and ModelingToolkit.jl in an efficient way so that these tools can be applied to modeling problems. To facilitate this goal, the basic concepts and syntax used in this tutorial is summarized below.

###  Functions illustrated:
<span style="font-family:Consolas; font-size:1em;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fill(), range(), collect(), sum(), round(), rand(),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; maximum(), max(), minimum(), min(), abs(), println(),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; typeof(), fieldnames(), Symbolics.value(), Symbolics.jacobian(),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Symbolics.jacobian_sparsity(), Symbolics.substitute()</span><br>

###  Metaprogramming macros illustrated: 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="font-family:Consolas; font-size:1em;">@time, @show, @doc, @variables, @parameters, @named</span>
<br>

###  Concepts illustrated:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;vector index notation<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;concatenation of vectors<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;function broadcasting<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;list comprehension<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dictionaries<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;begin/end blocks<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;garbage collection<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Just in Time (JIT) compiling<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;metaprogramming with macros<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;keywords in a function call<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;automatic type promotion<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;symbolic algebra<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;automatic differentiation<br>

###  Numerical algorithms illustrated:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Newton Raphson (from NonlinearSolve.jl)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Newton method with trust region (from NonlinearSolve.jl)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RobustMultiNewton (from NonlinearSolve.jl)<br>
