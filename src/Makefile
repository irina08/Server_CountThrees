# NAME: Student CS178 Irina Golovko
# FILE: Makefile 
# DATE: September 08, 2018
# Desc: A Makefile which build ServerCountThrees
# 		Make two directories on your VM; one called src 
# 		and one called data. Put the Makefile and 
# 		ServerCountThrees source code on your VM in the src directory
# 		Put the threesData.bin file in the data directory 
# 		Create a make target named "test" that:  
# 		a) creates a directory called 'build' in the same directory 
# 		as the src and data directories. 
# 		b) copies threesData.bin and ServerCountThrees 
# 		into the  build directory 
# 		c) launches the ServerCountThrees


# Assume that files in the 'scr' and 'data' directories
# are already unzipped and we are in the 'src' directory  

# Assign variables
CC=gcc
SrcDir=../src
NewDir=../build
DataDir=../data
files = ServerCountThrees.c readInt32BitLE.c 

# main target 'test' which depends on ServerCountThrees:
# Create dir 'build'
# copy threesData.bin from 'data' dir to 'build' dir
# copy executable 'ServerCountThrees' from 
# 'src' dir to 'build' dir
# go to the 'build' directory and execute ServerCountThrees
# Usage: make or make test
test: ServerCountThrees 
	mkdir $(NewDir) 
	cp $(DataDir)/threesData.bin $(NewDir)
	cp ServerCountThrees $(NewDir)
	cd $(NewDir) && ./ServerCountThrees	
	

# This target will compile all source files
ServerCountThrees:
	$(CC) -o ServerCountThrees $(files) 

# remove 'buld' dir and executable 'ServerCountThrees'
# from 'src' dir
# Usage: make clean
clean: 	
	-rm -rf $(NewDir) 
	-rm $(SrcDir)/ServerCountThrees
