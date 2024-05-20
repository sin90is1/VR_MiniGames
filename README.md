#VR Blueprint Crash Course

Developed with Unreal Engine 5 a full Bluprint project that is packaged for meta Quest 3 following the great course of "Unreal Engine 5 VR Blueprint Crash Course"

the link to the overview of this repo is (https://www.linkedin.com/posts/sina-ghavami-adel-b1b92a1b2_vr-gamedev-unrealengine-activity-7195905053931589633-uMXP?utm_source=share&utm_medium=member_desktop)

First of all, I had a lot of struggles working with the water plugin in Unreal Engine, especially when packaging and installing it for the Meta Quest. In the end, I found a solution for water in VR by following this method on YouTube: (https://www.youtube.com/watch?v=5B4b9Nk0GnM)

Initially, my problem was that the water material wouldn't render in VR and was not visible. The solution I found was to:

1.Check "Mobile HDR" in Project Settings/Rendering/VR and also turn off Instanced Stereo. By doing this, the water in water plugin will render, and the Post Process material and volume will work. However, this comes at a high cost, and I also encountered issues where my right eye was blank, and Quest recording didn't work.

2.Another approach is to use the "water_far" material that comes with the water plugin (just search for "far"). This will render the water. However, I faced a problem where, no matter how much I tried, I couldn't make the boat float correctly without going crazy, even when using the default Unreal mesh and following the documentation for the water plugin step by step. It would work on PC but not when installed on the Quest 3.(https://dev.epicgames.com/documentation/en-us/unreal-engine/water-buoyancy-component-in-unreal-engine?application_version=5.2)

In my opinion, the best way is to create the water using the YouTube video method and use the "water_far" texture/material for it (as it's just a simple plank). You can add floating movement in the Tick function.


