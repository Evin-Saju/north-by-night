# ✨✨ North by Night ✨✨
## The Idea: ##

North by Night is a mixed reality experience that teaches the learner how to recognize constellations and use them to find north. The night sky is projected onto the learner's own ceiling and walls using passthrough, so they learn in their own room. By the end, they should be able to walk outside on a clear night and find the North Star without help.

## What will the learner learn? ##

How to recognize key northern hemisphere constellations: the Plough (Big Dipper), Cassiopeia and Orion.\
How to use the pointer stars of the Plough to find Polaris, the North Star\
How to star-hop from one constellation to another\
Why the sky appears to rotate around Polaris over the night and through the year\
The myths and stories behind each constellation\

## How will they learn it? ##
  
### Step 1: Spot the Shape
The Plough appears on the ceiling with a short voice-over introduction. The learner points at each star in order to trace the shape, and the constellation lines draw themselves in as they go.
 
### Step 2: Pointer Stars
The two end stars of the Plough are highlighted. The learner drags a line out from these pointer stars and follows it across the sky to find Polaris, the North Star.
 
### Step 3: Star-Hopping
The learner is guided from Polaris to Cassiopeia, and from Orion's belt to Sirius. They hop from star to star using what they learned in the earlier steps.
 
### Step 4: The Moving Sky
A star wheel appears in the learner's hand. They grab and rotate it to change the month and hour, and watch the whole sky turn around Polaris. This shows why it is the one star that stays still.
 
### Step 5: Lights Out (Final Test)
All lines and labels are hidden, and a voice asks the learner to "Find north". They have to find Polaris from memory, and are scored on time and accuracy.
 
**Feedback:** correct answers trigger a chime, particles and a haptic pulse. Wrong answers give a hint, such as briefly flashing the correct star or replaying the last step. Progress and scores are shown on a floating 3D UI panel.

## Technology and Libraries ##
 
| Technology | What it is used for |
|------------|---------------------|
| **Godot 4 + OpenXR** | Engine and XR runtime |
| **[Godot OpenXR Vendors](https://github.com/GodotVR/godot_openxr_vendors)** | Passthrough, hand tracking, and the Meta Scene SDK (finding the ceiling and walls to place the sky and compass directions) |
| **[Godot XR Tools](https://github.com/GodotVR/godot-xr-tools)** | Pointer function for selecting stars, pickables for the star wheel and chart, 3D UI viewports |
| **[Hand Pose Detector](https://github.com/Malcolmnixon/GodotHandPoseDetector)** | Open palm and fist gestures for revealing and hiding constellation artwork |
| **Shaders** | Twinkling stars, glowing constellation lines |
| **Tweens / AnimationPlayer** | Lines drawing in, artwork fading in, sky rotation |
| **GPU Particles** | Feedback effects when the learner gets an answer right |
| **Spatial Audio** | Voice-over and myths played from each constellation's position, plus ambient night sounds |
| **Timers** | Scoring the final challenge |
| **Signals** | Communication between stars, levels and the UI (for example `star_selected` and `level_complete`) |
