# JCIM_codes
Codes used in "Kinetic barrier to enzyme inhibition is manipulated by dynamical local interactions in E. coli DHFR" paper

# Figure 4

Codes for extracting timewise distance information. Use it after aligning the structure. 

for tcl: source codename.tcl
for python : for each system (active site residues for WT and L28R) make sperate folder for each and place the python code inside. The code will be calculating the averages and standard deviations for the system. 

# Figure 6

Timewise barcode graphs.

hbond_measuring_code : source the file. It will extract the timewise hydrogen bonding profile of the ligand with the protein. 
index_extraction : source the file. It will extract the index ids used in hbond_measuring_code for each atoms of protein and the ligand. 
occupancy&barcode : after having the outputs of hbond_measuring_code & index_extraction scripts run the file for occupancy first. Then from the listed occupancies if you like to extract barcode information uncomment barcode line in the script. Use the occupancy naming and numbering as it exemplified in the script. 

# Figure 8

Hydrogen bonding information and their difference from the wild-type system.

First extract hbond data from the VMD Timeline Plugin. Use index_extraction to get the protein indexes.

Give 2 files as input to hydrogen_bond_enzyme.py. Note that you have to have 5 pairs of these files since the microsecond trajectory is chopped to five. In wt_occ, the program will calculate the avegare occupancy of these five chunks for each hydrogen bonding and compare it with the target system.

Run the to code for 0 difference in line 185 to get the difference information. You may run a frequency distribution analysis elsewhere to calculate how many sigma defines your treshold. Then you can change line 185 to this number to get the only significant hydrogen bonding information. 

# Figure S4

Root mean squeared fluctuations (RMSF).

source rmsf.tcl to get the RMSF values. 

# Figure S6

Cross-correlation maps.

Make different folders for each ligand. Place the the mutant systems (pdb and dcd files) to this folder (WT and L28R in this case). Then place the cross_corr (cross correlation) code for corresponding ligand into the that folder. The code will generate cross-correlation images for the systems you placed into.  

