# VRTemplate_TAndL

Developed with Unreal Engine 5

First of all, I had a lot of struggles working with the water plugin in Unreal Engine, especially when packaging and installing it for the Meta Quest. In the end, I found a solution for water in VR by following this method on YouTube: [YouTube Link].

Initially, my problem was that the water material wouldn't render in VR and was not visible. The solution I found was to:

1.Check "Mobile HDR" in Project Settings/Rendering/VR and also turn off Instanced Stereo. By doing this, the water in water plugin will render, and the Post Process material and volume will work. However, this comes at a high cost, and I also encountered issues where my right eye was blank, and Quest recording didn't work.

2.Another approach is to use the "water_far" material that comes with the water plugin (just search for "far"). This will render the water. However, I faced a problem where, no matter how much I tried, I couldn't make the boat float correctly without going crazy, even when using the default Unreal mesh and following the documentation for the water plugin step by step. It would work on PC but not when installed on the Quest 3. [Water Buoyancy Component Documentation.]

In my opinion, the best way is to create the water using the YouTube video method and use the "water_far" texture/material for it (as it's just a simple plank). You can add floating movement in the Tick function.


