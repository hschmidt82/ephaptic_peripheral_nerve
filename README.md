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


# Update 20 May 2022:

The manuscript is now published: https://doi.org/10.1007/s00422-022-00934-9

Thanks to the reviewers’ keen eyes, the manuscript has undergone some substantial improvements compared to the biorxiv version. The file “SPM_final_diff.tar.gz” contains all files necessary to recreate the changes in the figures:

Fit_a1.m creates Figure 3b, loads Fit_Profile.mat

Fit_Pars2.m creates Figure 3c, loads Fit_Delays_N10_v2.mat

Figure3d.m creates the panels in Figure 3d, requires fSpikeProp (from original submission)

Figure3e.m creates Figure 3e, requires fCable_biophys3.m

Figure4d.m creates the panels in Figure 4d, loads Fig4cdrev_delay_N200.mat

Figure5d creates the panels in Figure 5d, loads Fig5cdrev_delay_N200.mat

Screen_Cable_biophys_large.m creates the results for Figure 6b, requires fCable_biophys2.m

Quad_approx.m generates the results for “SPM” in Figure 6c, requires fQuad_approx.m

Cable_eph_theor_2.m generates the results for “biophysical” in Figure 6c, requires fCable_eph_theor_2.m and loads Cable_passive.mat
