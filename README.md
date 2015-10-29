# whetstone_leon
Adaption of whetstone baremetal benchmark to work with LEON3 microprocessor

Modifications made by LIS, marked with ```//#LIS# Start LIS Modifcation``` and ```//#LIS# End LIS Modifcation```.
Local variables have been replaced by global variables.

# Usage on linux bash
	
- Variant 1: ```whetstone 100000``` - 100000 is the number of loop iterations
- Variant 2: ```whetstone -c 100000``` - this will run the benchmark continiously with 100000 loop iterations for each run
	
# Usage in LEON3
- Copy the cody from ```whetstone.c``` into the file ```systest.c``` within your __design__ folder.
- Modify the file ```software/leon3/Makefile```: Search for line starting with __LDFLAGS__ and add ```-lm``` at the end of the line. This will link the library __math.h__ that is needed by the whetstone benchmark. 
	
