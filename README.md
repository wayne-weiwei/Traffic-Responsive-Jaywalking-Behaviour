# Traffic-Responsive-Jaywalking-Behaviour
# Closed-Loop Comparison Videos: Generated vs. Scripted Jaywalkers in CARLA

Supplementary videos for the paper **Generating Traffic-Responsive Jaywalking Behaviour via Flow Matching**
(Wei Wei, Yuxuan Han, Zihan Liu, Jiaying Xue, Yu Feng, and Jianglin Lan; submitted to IEEE Transactions on Intelligent Transportation Systems).

The clips come from closed-loop tests on Bench2Drive pedestrian-crossing routes in CARLA 0.9.15 with three published driving models: PDM-Lite, the TransFuser policy of LEAD, and SimLingo. Our generated pedestrian replaces the scripted Bench2Drive pedestrian at the same spawn point, occluder, and trigger.

## Video Layout and Labels

**Clips 1–6:** Each clip has two rows. The top row shows the original scripted pedestrian from Bench2Drive, and the bottom row shows our generated pedestrian (Ours). Both use the same driving model and route, with time aligned to the pedestrian trigger (t = 0).

**Clip 7:** Three rows show the same generated pedestrian (with the same random seed) interacting with PDM-Lite, LEAD, and SimLingo.

Each row contains:

- **Views:** Third-person chase view on the left and bird's-eye view on the right. For SimLingo, its own camera input is also shown.
- **Status bar:** Vehicle speed, pedestrian speed, and vehicle–pedestrian distance.
- **Labels:** BOTH WAITING (the vehicle and the pedestrian are both stopped while the pedestrian is on the road), walker stopped on road, ego stopped, and COLLISION.
- **Bottom plots:** Vehicle speed (blue), pedestrian speed (orange), and vehicle–pedestrian distance. Orange shaded areas indicate periods when both are waiting, and red lines mark collisions. SimLingo's language outputs are also displayed.

## Clip Descriptions

### 1. PDM-Lite


https://github.com/user-attachments/assets/27c4b592-050d-473e-9c48-2db4c6c7a9f2


**Original pedestrian:** The pedestrian crosses at a constant speed of 2 m/s. PDM-Lite slows down but does not stop. At t = 2.65 s, an oncoming vehicle in the opposite lane hits the pedestrian. On this route, the scripted pedestrian is hit by another vehicle in all ten runs.

**Ours:** The pedestrian stops near the road centre line, and PDM-Lite stops at a minimum distance of 1.3 m. Both wait for 6.55 s, and the vehicle restarts three times. The pedestrian remains on the road for 12 s, and no collision occurs.

### 2. LEAD


https://github.com/user-attachments/assets/ed6d58a4-9819-412d-be33-e3a43fec79e9


**Original pedestrian:** LEAD stops for 2.75 s, and the pedestrian completes the crossing within 2.75 s. No collision occurs.

**Ours:** The pedestrian stops in the driving lane, and LEAD stops as well. Both wait for 12.95 s, and LEAD does not pass until 20.7 s. The minimum vehicle–pedestrian distance is 6.6 m.

### 3. SimLingo


https://github.com/user-attachments/assets/83818551-51ac-4f2f-95e1-7cc139d26ada


**Original pedestrian:** SimLingo does not stop for the pedestrian.

**Ours:** The pedestrian stops in the lane for 8.9 s. SimLingo first states "Decelerate due to the pedestrian intersecting your path" but later describes the pedestrian as a bicycle to follow ("follow the maroon bicycle"). The vehicle restarts 17 times, gradually approaching the pedestrian, and hits the pedestrian at t = 13.0 s as the pedestrian starts moving again.

### 4. PDM-Lite


https://github.com/user-attachments/assets/e6e4395c-46d3-429f-b9a0-4b9ddcb66b87


**Original pedestrian:** PDM-Lite stops for 1.1 s, and the pedestrian completes the crossing in 2.6 s.

**Ours:** The vehicle and the pedestrian wait for each other for 12.5 s. PDM-Lite restarts seven times and does not pass until 21.4 s. No collision occurs.

### 5. LEAD


https://github.com/user-attachments/assets/cbc1a427-bc71-417a-82a9-fe312e35d1ff


**Original pedestrian:** The pedestrian appears from behind a rock or billboard and is hit at t = 1.95 s.

**Ours:** The generated pedestrian appears from behind the same obstacle and is hit at t = 2.1 s. Both pedestrians are hit at this location because the obstacle blocks the vehicle's view; the collision is not caused by the pedestrian model.

### 6. SimLingo (Night)


https://github.com/user-attachments/assets/dccad8af-a652-4bbe-a157-154b3a655152


**Original pedestrian:** SimLingo slows down but does not stop and passes the pedestrian at a minimum distance of 3.9 m without a collision.

**Ours:** The pedestrian stops in the ego vehicle's lane. SimLingo stops about 6 m away but describes the pedestrian as a "blue bicycle" or "maroon bicycle". It then restarts 11 times while moving forward. At t = 10.5 s it states "Pay attention to the walker", but it hits the pedestrian at t = 10.9 s. This is the same type of failure as in Clip 3, on a different route.

### 7. Same Generated Pedestrian with Three Driving Models


https://github.com/user-attachments/assets/01eca3a4-24e0-4ac8-8003-9a9b267bc2ae


All three driving models meet the same generated pedestrian (same random seed), who walks towards the road centre line.

**LEAD:** LEAD stops early, about 7.3 m from the pedestrian. The pedestrian steps back by about 0.7 m, and both wait for 10.8 s. The pedestrian moves first, and LEAD does not pass until 19.7 s.

**PDM-Lite and SimLingo:** Both models stop or slow down and then pass while the pedestrian is still standing in the opposite lane, at minimum distances of 1.4 m and 1.3 m, respectively. Both vehicles stop again at t = 12 s because of a red traffic light ahead, not because of the pedestrian.
