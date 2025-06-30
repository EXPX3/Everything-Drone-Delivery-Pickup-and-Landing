# Everything-Drone-Delivery-and-Landing
References to or implementations of algorithms &amp; benchmarking framework related to Drone Delivery and landing.  

# No universal Drone delivery and landing algorithm. Shall be tailored specifically for usecase. 
## Popular usecases already thriving in real-world scenarios are
1. last mile cargo delivery
2. Emergency landing modes
3. Military deployments
4. Indoor environments
5. ...

## Perception capabilities of the Drone to achieve autonomous delivery and landing
1. camera - images
2. LiDAR - depth
3. DTM/DEM/GIS prior information
4. spectral data ?

## Types of algorithms and what they analyze
1. Mathematical models and preset heuristic rules - point cloud data as input - for gemoetric terrain charecteristics analyisis ex: slope, roughness, obstacle offset, point density and size of the Delivery / landing areas.
   - Drawbacks: lack of semantic information of terrain objects like water, complex unstable flat surface etc
   - Positive: simple and computationally cheap
2. Image processing-based methods - images as input - for visual edge, pattern, texture analyisis ex: uniform region in an image may point to flat region, edges may highlight boundaries etc.
   - Drawbacks: performance directly depend on lighting and altitude, manual parameter tuning, do not guarentee optimal perfomance
   - Positive:  cheap hardware
3. AI based methods:
   - image based DL:
   - Lidar based DL:
   - image+Lidar based DL:
4. New sensible potential combinations of above methods.

## Benchmarking 
1. Opensourced Data sets with ground truth information: algorithms can be tetsed on this commonly available dataset and publish performance results.
2. Monte-Carlo simulations:
