# Traffic-Responsive-Jaywalking-Behaviour
Supplementary videos for the paper

**Generating Traffic-Responsive Jaywalking Behaviour via Flow Matching**
Wei Wei, Yuxuan Han, Zihan Liu, Jiaying Xue, Yu Feng, and Jianglin Lan
*Submitted to IEEE Transactions on Intelligent Transportation Systems.*

The videos show closed-loop tests on Bench2Drive pedestrian-crossing routes in CARLA 0.9.15 with three published driving stacks: PDM-Lite, the TransFuser policy of LEAD, and SimLingo. Our generated pedestrian replaces the scripted Bench2Drive pedestrian at the same spawn point, occluder, and trigger.

**How to read the videos**

- Clips 1–6: top row = scripted Bench2Drive pedestrian; bottom row = generated pedestrian (ours). Both rows use the same driving stack and route and are aligned at the scenario trigger (t = 0).
- Clip 7: one generated pedestrian (same random seed) meets PDM-Lite, LEAD, and SimLingo.
- In each row: left = chase camera, right = top-down view (for SimLingo, its camera input). The status bar gives vehicle speed, pedestrian speed, and vehicle–pedestrian gap. Badges mark mutual waiting, a pedestrian stopped on the road, a stopped vehicle, and collisions. The plots show vehicle speed (blue), pedestrian speed (orange), and the gap; orange shading marks mutual waiting and a red line marks a collision. For SimLingo, its language output is shown.

---

### Clip 1 — PDM-Lite, route jw_64: mutual waiting

The scripted pedestrian walks straight across and is struck by an oncoming vehicle in the opposite lane. The generated pedestrian stops near the centre line; PDM-Lite stops, and both wait before the crossing continues without a collision.

<!-- drag 01_PDM-Lite_jw64_mutual-waiting.mp4 here -->

### Clip 2 — LEAD, route jw_145: mutual waiting

The scripted pedestrian crosses within a few seconds. The generated pedestrian stops in the lane; LEAD stops, and the two wait for each other before LEAD passes.

<!-- drag 02_LEAD_jw145_mutual-waiting.mp4 here -->

### Clip 3 — SimLingo, route jw_145: stopped pedestrian, collision

SimLingo passes the scripted pedestrian without stopping. The generated pedestrian stops in the lane; SimLingo first reports the pedestrian, then describes it as a bicycle to follow, repeatedly restarts, and strikes the pedestrian.

<!-- drag 03_SimLingo_jw145_stopped-pedestrian-collision.mp4 here -->

### Clip 4 — PDM-Lite, route jw_146: stop-and-go

The scripted pedestrian crosses quickly after a short vehicle stop. With the generated pedestrian, PDM-Lite and the pedestrian wait for each other, and the vehicle starts and stops several times before passing, without a collision.

<!-- drag 04_PDM-Lite_jw146_stop-and-go.mp4 here -->

### Clip 5 — LEAD, route jw_147: occluded pedestrian, collision with both pedestrians

On this route the pedestrian appears from behind an occluder, and LEAD strikes both the scripted and the generated pedestrian shortly after the trigger. The collision is caused by the occlusion on this route rather than by the pedestrian model.

<!-- drag 05_LEAD_jw147_occluded-pedestrian-collision.mp4 here -->

### Clip 6 — SimLingo, route jw_122 at night: stopped pedestrian, collision (Fig. 7b)

SimLingo passes the scripted pedestrian without a collision. The generated pedestrian stops in the ego lane; SimLingo stops about 6 m before it, describes it as a bicycle to follow, restarts repeatedly, and strikes it.

<!-- drag 06_SimLingo_jw122_night-collision_Fig7b.mp4 here -->

### Clip 7 — Route jw_64: one generated pedestrian, three driving stacks (Fig. 7a)

The same generated pedestrian reaches the centre line. LEAD stops early; the pedestrian steps back, both wait, and the pedestrian crosses first. PDM-Lite and SimLingo stop or slow down and then pass while the pedestrian stands in the opposite lane. The later vehicle stops are caused by a red light ahead, not by the pedestrian.

<!-- drag 07_three-stacks_jw64_same-pedestrian_Fig7a.mp4 here -->
