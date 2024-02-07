# IFCB: Carbon Mass to Volume Conversion
Based on regressions from _[Menden-Deuer and Lessard (2000)](https://doi.org/10.4319/lo.2000.45.3.0569)_ estimate the carbon mass of a protist from its biovolume.

__Processing__:
- Biovolume data comes from the V4 feature extraction Matlab routine.
- Pixel volume is converted to um^3 using the pixel conversion factor of 1/2.77 microns per pixel
- Total biovolume for each class is calculated and normalized to the sample volume in mL.
- Total biovolume is converted to biomass in Carbon (pg C) using the following regressions:
  - __Diatom__:    $ pgC \ cell^{-1} = 0.288\  X \ volume^{0.811} $  
  - __All Protists Excluding Diatoms__:   $ pgC \ cell^{-1} = 0.216\  X \ volume^{0.939} $   