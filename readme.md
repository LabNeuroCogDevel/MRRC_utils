# LNCD utilities for MRRC

##  `task_presentation/waitForScannerTrigger.m` 
This is a MATLAB+PTB function to wait for a scanner triggered fast simulated keypress, in our case, sent via Psychology Software Tools' button box.
It uses `KbQueue` because the simulated keypress is too fast to be consistently captured by `KbWait` or `KbCheck`. 

Written to adapt the frogger and rest/calibration tasks in mMR after button box update, 2018-01-03.

## slice annotation warping graphical interface
This GUI was written to acquire a consistent slice defined in MNI space. It is used in the 7T. 
DICOM conversion matlab code is from Chan-Hong Moon.
https://github.com/LabNeuroCogDevel/slice_warp_gui

## protocol consistency 
Siemens acquisition software includes a "feature" that reverts protocol settings.
An after the scan check is preformed on a sqlite database created from DICOM headers:
https://github.com/LabNeuroCogDevel/mrproto_sql.git

