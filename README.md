**RS-PestDyn**

This is a python code of insect pest population dynamics model, which currently simulates one life stage of a generic insec pest for a single day. The model uses a numerical solution for the differential equation of age distribution through a the  Runge-Kutta method. The main driver of this model is temperature. The satellite-derived land surface temperature product of MODIS (1km, daily) is used as input to the model.

Main program to run:
'run_RK4_2D.py'

Procedures called (3):
'Download_Temp_GEE.py' - download TIF files of LST from MODIS as a batch from GEE
'RK4_2D_procedure.py'  - solves the ode using Runge-Kutta
'display_plots.py'     - displays results (as a 2D matrix of % population)

Needs:
1) extend to entire period (currently for 1 day)
2) extend to other life stages (currently only 1)
3) improve solution for error expansion through time.
4) add LC/LU classification
5) add plant growth
6) add migration between pixels
