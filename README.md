# CAGEO-1D-IVA
Overview of the 1D VES Forward Modelling & Inversion Toolkit
Using the Schlumberger electrode configuration, this repository offers a Python-based implementation for forward modelling and inversion of Vertical Electrical Sounding (VES) data. 

# The framework is intended for: 
- Precise modelling of apparent resistivity responses across layered earth models 
- Sturdy inversion of synthetic and field VES datasets 
- Estimating stable parameters with sophisticated numerical optimisation methods 
The inversion method incorporates Singular Value Decomposition (SVD) into a nonlinear least-squares framework to guarantee subsurface resistivity model convergence, stability, and dependability.

# Features
- Multilayer earth resistivity using 1D forward modelling 
- SVD-based optimisation for iterative inversion
- Assistance with changing resistivity and fixed layer thickness 
- Dual misfit assessment: 
  - Linear-domain NRMS error (accuracy of data fitting) 
  - Error in the logarithmic domain (inversion control and stability) 
  - The normalised data misfit assessment's weighted RMS (WRMS) error (%) 
- Iterative updates with convergence control and damping 
- Plotting at high resolution (figures suitable for publication) 
- Compatibility with field and synthetic datasets

# Approach: 
Forward Modelling
Standard Schlumberger assumptions are used to calculate apparent resistivity for a horizontally stratified earth model. The input layer thicknesses and resistivities are used to construct the forward response. 

# Inversion Technique 
- The resistivity and thickness parameters define the initial model. 
- SVD-based least squares are used to update model parameters iteratively. 
- Damping is used to keep the inversion process stable. 
- Iterations continue until the convergence requirements are met. 

# Misfit Features 
1. NRMS Error Linear: assesses the linear domain's absolute data misfit. 
2. Error in Logarithm: maintains convergence over various resistivity scales and regulates inversion updates. 
3. Error (%) of Weighted RMS (WRMS): A normalised estimate of the discrepancy between calculated and observed apparent resistivity values is provided by the WRMS error:

# This measure is employed to: 
- Calculate the precision of inversion
- Examine model performance in various datasets. 
Evaluate the robustness of convergence.

# Results 
- Models of inverted resistivity
- Plotting NRMS errors on both linear and logarithmic scales 
- Each iteration's WRMS error (%) Convergence curves 
- 300 DPI exported figures that are appropriate for publication


# Verification 
The following methods have been used to validate the algorithm:
- Artificial multilayer earth models 
- Comparing benchmarks with accepted inversion techniques
- Field datasets for practical use


