# Kalman-Filter

Here is the WIP repo for our Sensor fusion. It basically uses IMU data to improve Lighthouse positioning dynamism.
This repo also contains the 3d models of the structure, helpful for the calibration algorithms for example...

There are 3 kinds of files:
  - Data preprocessing: transforms accelerations from IMU and Lighthouses data into 3D points.
  - Sensor fusion: this Kalman Filter (and more variations in progress) estimates the tracker position as well as possible.
  - Visualization: this Blender file uses position calculated after Sensor fusion.
  
Prerequisites:
  - Python libraries used are all in the Anaconda package: https://www.anaconda.com/download/.
  - Serial library can be found here: https://github.com/pyserial/pyserial/
  - Find Blender on their website: https://www.blender.org/download/
  
Enclosures options:
  - Main enclosure: 4 arms and 1 body frame.
  - Tetraedron: it allows visibility for at least one diode in any orientation.
  
Simulation:
On the Dev branch, a mini-game simulation is in LH_Simu.blend, see the Python script inside.
You can move the blue car with Z, Q, S, D key (Because of french keyboard), and the scanning/calculated position will appear with a green dot.

Calibration:
  There is also an other way of calculating position from the Lighthouses. It use the assumption that Diodes are on a solid frame (our main enclosure). This Python code allows to know position and orientation of Lighthouses but isn't accurate enough for the moment. A visualization of the calculated points is also in the folder.
