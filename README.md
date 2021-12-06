# ephaptic_peripheral_nerve

Short Description:

This code was developed under MATLAB version R2021a, and utilises standard functions that should be available in other MATLAB versions. Some scripts use the Parallel Toolbox. If it is unavailable, replace the ‘parfor’ loops by standard ‘for’ loops.

For a detailed description of the background and the Figures the code produces, see the following manuscript: https://doi.org/10.1101/2021.11.30.470540 

Files:


- Biophysical_Example.m

This file generates the data for Figure 1a, and it also creates the ‘Cable_passive.mat’ file used by the following file.


- Cable_eph_theor.m

This file generates Figures 1b and 1c.


- Quad_approx.m

This file generates Figures 2a, 2b, and 2c.


- Screen_Cable_biophys.m

This file generates the data to which the spike propagation model is fitted. It calls the function ‘fCable_biophys.m’. The data are stored in ‘Fit_Delays.mat’, which is used by the following file.


- Fit_pars.m

This file fits the parameters of the spike propagation model by screening the parameter space and computing the cost function. It calls the function ‘fSpikeProp.m’, which in turn calls the function ‘fPropFun.m’. Figures 3b and 3c are produced by this file.


- Figure4ab.m

This file generates Figures 4a and 4b. It calls the function ‘fSpikeProp.m’. By replacing ‘uniform’ in line 58 by ‘alpha’, this file produces Figures 5a and 5b instead.


- Figure4cd.m

Produces Figures 4c and 4d. If drvec is set to 0.03 in line 6, and ‘uniform’ is changed to ‘alpha’ in line 58, then this script produces Figures 5c and 5d.
