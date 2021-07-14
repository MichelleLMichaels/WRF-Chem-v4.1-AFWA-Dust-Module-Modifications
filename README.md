# WRF-Chem-v4.1-AFWA-Dust-Module-Modifications
AFWA dust emissions module code modifications adapted for WRF-Chem v4.1

The drag partition modified code located here applies an albedo-based drag partition parameterization into the AFWA (Air Force Weather Agency) dust emissions module that is implemented into WRF-Chem v4.1. 

Please refer to Michelle Michaels ERDC Special Report SR-20589 for more information. Included code in this repository is listed below:

-registry.chem: file to add namelist variables

-chem_driver.F: passes uns* data to the AFWA dust emission module 

-emissions_driver.F: passes uns* data to the AFWA dust emission module 

-module_gocart_dust_afwa.F: AFWA dust module containing uns* modified code

Note: To use the WRF-Chem dust drag partition scheme, copy the .F files within each subfolder to the corresponding subfolder within the main WRF-Chem Directory and recompile.  Note that because there is a change made to the registry, you will need to do a full clean of WRF-Chem in order for the new scheme to be compiled correctly.
