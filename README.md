# Everything-Drone-Delivery-Pickup-and-Landing.
# NOTE: Work in Progress, Feel free to make any suggestions, remarks via github issues. 
Purpose of this repo is to keep track of academic research and realworld adoption of Drone delivery, pickup and landing technology. Expect, open-source implementations, publications, interviews etc any media relavant to the topic.  

# No universal Drone delivery , pickup and landing algorithm. Shall be tailored specifically for usecase. 
## Popular usecases already thriving in real-world  ...
1. Last Mile Drone Delivery Ex: [wing](https://wing.com/), [Flytrex](https://www.flytrex.com/), ... (list will be updated to include all note worthy drone delivery companies and capabilities like payload, flight time, distance coverage etc.. )    
2. Hub to Hub Delivery
3. Disaster response / Search and Rescue
4. Remote location delivery drones Ex: High altitudes, sparsely populated areas, Long distances travel etc.
5. ... 

## Common requirments for Delivery & Pickup Drone Operations:
1. Designated / Regulated Flying corridors ?
2. Emergency Safe Landing
3. Drone traffic handling ?
4.  ...

 
## Perception capabilities of the Drone for Delivery, Pickup and landing, state of the art and future ...
1. camera - images
2. LiDAR - depth
3. DTM/DEM/GIS prior information
4. spectral data ?
5. high resolution radar ?

## Types of Drone Delivery and landing zone detection algorithms and what they analyze ...
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

## Benchmarking 
1. Opensourced Data sets with ground truth information: algorithms can be tetsed on this commonly available dataset and publish performance results.
2. Monte-Carlo simulations based benchmarking (implementation available - cosmetics ):  for each hazard metric independently, adjusting its value across the acceptable-to-unacceptable range while maintaining other metrics within thresholds. Thresholds for hazard metrics, such as relief, roughness, slope, radius, and point density, are determined based on the UAS’s landing gear ground clearance, maximum offset from surroundings, and intended operating height. Doing so the edge case behaviour of the Delivery / Landing zone detection method is studied with an aim of evaluating the algorithm for its success rate, computation time and memory in the current implementaion.
3. ...
