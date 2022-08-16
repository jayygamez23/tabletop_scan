# 3D Tabletop Scanner

##Simple tabletop 3D object detector using PCL

This project takes in a pcd file called "tabletop.pcd" from a Intel RealSense looking down on a tabletop surface. The code does the following: 
- Filters the point cloud in a pipeline with a Passthrough and Voxel Grid filter
- Colors the tabletop blue (Found using plane segmentation)
- Finds clusters above the tabletop
- Colors any found boxes green 
- Colors spherical objects red
- Visualizes the point cloud with a wrapper class (CloudVisualizer.cpp)
- Creates an output.pcd file to be viewed if needed

## How to Compile
1. Make sure your machine has PCL 1.8 installed and all of its dependencies. 
2. Create a build folder for cmake and make commands for organization purposes
3. Inside the build folder, use `cmake ..` to generate the build files and `make` to compile the program. 
   - You can also compile with threads for a faster compilation, ex: `make -j2`
4. Run with `./tabletop_scan ../tabletop.pcd`
