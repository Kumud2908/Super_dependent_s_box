# Super_dependent_s_box
Q1- for n=2 number fo supere dependent s_box=0
for n=3 number of supre depnedent s_box=24576
for n=4  i have written the code for finding the number of boxes but jupyter notebook is not able to execute it 
Q2-there are 0 s-boxes
Q-3- i have shown the output for n=3 and given the code for n=4 
Q-4- For an arbitrary n, the approach can be generalized as follows:

1.Vectorial Boolean Functions for n-bit Inputs:
  >> For n-bit inputs, you generate all possible Boolean functions by varying the coefficients c1,c2,c3....c2^n-1 in an algebraic expression representing the Boolean function.
  >> Each Boolean function has 2^n inputs (all possible combinations of n binary variables) and produces a single output bit.

2.Dependency Check on All Variables:
  >> After generating each Boolean function, you check if the function depends on all n input variables. This can be done by verifying that changing any input bit affects
   the function's output (for example, by comparing pairs of outputs where only one input bit differs).
  >> This is done using a generalized version of the is_dependent_on_all_variables function, which checks each input variable.

3.S-Box Construction:
  >> To construct an S-box, you select n Boolean functions from the list of functions that depend on all variables. Each of these functions will generate one bit of the n-bit
    output for each 𝑛-bit input.
  >>You check whether the outputs of these functions form a permutation of all possible n-bit values  i.e., [0,1,...2^n-1] for all input combinations.

4.LAT and DDT Calculation:
  >> Compute the Linear Approximation Table (LAT), which measures the linear biases between the input and output bits.
  >> Compute the Difference Distribution Table (DDT), which measures how differences in inputs affect differences in outputs (useful for analyzing differential cryptanalysis resistance).

5.Evaluating Nonlinearity and Differential Uniformity:
  >> Nonlinearity is evaluated based on the maximum entry in the LAT (it indicates how far the function is from being affine).
  >> Differential Uniformity is evaluated based on the maximum entry in the DDT (it indicates how uniformly the S-box spreads differences in the inputs).

   

   

