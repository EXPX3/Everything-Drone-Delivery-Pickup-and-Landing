# Everything-Drone-Delivery-Pickup-and-Landing.
# NOTE: Work in Progress (WIP), Feel free to make any suggestions, remarks via github issues / pull requests. 
Purpose of this repo is to keep track of academic research and realworld adoption of Drone delivery, pickup and landing technology. Expect, implementations and references to open-source contributions, publications, interviews etc any media relavant to the topic.  

# No universal Drone delivery , pickup and landing algorithm. Shall be tailored specifically for usecase. 
## Popular usecases already thriving in real-world  ...
1. Last Mile Drone Delivery Ex: [wing](https://wing.com/), [Flytrex](https://www.flytrex.com/), ... (list will be updated to include all note worthy drone delivery companies and capabilities like payload, flight time, distance coverage etc.. )    
2. Hub to Hub Delivery
3. Disaster response / Search and Rescue
4. Remote location delivery drones Ex: High altitudes, sparsely populated areas, Long distances travel etc.
5. ... 

## Common requirments for Delivery & Pickup Drone Operations:
1. Designated / Regulated Flying corridors / Drone traffic handling ?
2. Landing Delivery Zone Detection
3. Emergency safe Landing strategies
4. ...


 
## Perception capabilities of the Drone for Delivery, Pickup and landing, state of the art and future ...
1. camera - images
2. LiDAR - depth
3. DTM/DEM/GIS prior information
4. spectral data ?
5. high resolution radar ?
6. ...

# Algorithms & Benchmarking strategies
## Types of Drone Delivery and landing zone detection algorithms ...
1. Mathematical models and preset heuristic rules - point cloud data as input - for gemoetric terrain charecteristics (Hazard metrics) analyisis ex: slope, roughness, obstacle offset, point density and size of the Delivery / landing areas.
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
5. ...

## Benchmarking 
1. Opensourced Data sets with ground truth information: algorithms can be tetsed on this publicly available datasets and publish performance results. Example datasets: [ECLAIR: A High-Fidelity Aerial LiDAR Dataset for Semantic Segmentation](https://github.com/SharperShape/eclair-dataset), [MUN-FRL: Aerial Visual-Inertial-LiDAR Odometry and Mapping Dataset](https://mun-frl-vil-dataset.readthedocs.io/en/latest/), [MARS-LVIG Dataset: A multi-sensor aerial robots SLAM dataset for LiDAR-visual-inertial-GNSS fusion](https://mars.hku.hk/dataset.html), ...
2. Monte-Carlo simulations based benchmarking (implementation available):  for each hazard metric independently, adjusting its value across the acceptable-to-unacceptable range while maintaining other metrics within thresholds. Thresholds for hazard metrics, such as relief, roughness, slope, radius, and point density, are determined based on the UAS’s landing gear ground clearance, maximum offset from surroundings, and intended operating height. Doing so the edge case behaviour of the Delivery / Landing zone detection method is studied with an aim of evaluating the algorithm for its success rate, computation time and memory in the current implementaion. [Algorithms & Benchmarking strategies](https://github.com/EXPX3/Drone-Delivery-Landing-Zone-Detection)
3. ...
