# JAVA iCASA WORKSPACE

The files in this repository contains my personal code for iCasa simulation software.

Author:
Pasquale Roseti

The scripts folder contains the scripts usable with the software:
- room_ext.bhv : script for a single room environment
- paper_script.bhv : script for a multi-room environment
The program runs with both the scripts, just remember to change the name of the dataset file when changin environment, if you want to not override it.
It is possible to change it in the datasetManager\src\iCasa\dataset\manager\datasetManagerImpl.java file.


# Simulation

In order to run a simulation we need to download the iCasa software to http://adeleresearchgroup.github.io/iCasa/snapshot/index.html. 
The package will provide some files and directories which we can use to run the software.
In particoular:
- applications: folder in which to put the bundles we want to deploy (a bundle is a JAVA code which runs the logic of the environement, modelling the behaviours of the devices).
- scripts: contains the scripts we want to use for simulation. The list of these scripts will be available from the user interface.
- startGateway (.bat or .sh, depends on your operating system): it launchs the whole simulator, so it deploys the bundles and make us able to access the user interface at http://localhost:9000/simualtor.

Now, if we navigate to http://localhost:9000/simualtor, we have access to the simulation platform, from which we can control devices, person and so on.

Step to run a simulation:
1. Insert environment script file into scripts folder
2. Deploy required bundles to manage device logic
3. Access to http://localhost:9000/simualtor and run the script

Now, we can interact with the simulation both directly via browser or even by code (with proper HTTP APIs).

The DevicePropertyAPI folder contains the classes to build a REST API that interacts with iCasa devices.