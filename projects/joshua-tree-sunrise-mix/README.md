# Joshua Tree Sunrise Mix

A one-hour DJ mix recorded in Joshua Tree.

The source performance was filmed from a 360 camera mounted to a truck. I sat in the truck bed and DJ'd while a friend drove through the desert.

## Vision

Release the mix as a video that treats the drive, the truck, my body, and the landscape as separate visual surfaces.

The core idea is to mask my body using Meta's Segment Anything Model (SAM), then apply audio-reactive effects to that body mask. The effects should feel attached to the performance rather than pasted over the footage.

## Conceptual Frame

Older notes describe this project as a "Mediated Renderer": a way to render the mix, the drive, the memory, and the music's meaning into one visual system.

The video should not be a decorative visualizer laid on top of footage. The goal is to visualize a transition from physical travel through Joshua Tree into a mediated world. The drive acts as a marker for returning to orientation during a strange, chaotic period.

Design priorities from the notes:

- Treat the details and complexity as the art.
- Treat the movement of the mediation as the art.
- Let visual effects have reasons inside the world, not just aesthetic reactions.
- Use the music as structure: track, transition, energy, and spectrum should all be available as visual inputs.
- Preserve the sense that this is a continuous journey rather than a collection of unrelated clips.

## Basis / Mediated.World Rules

This project should obey the philosophy of `basis` and `mediated.world`, not just borrow the aesthetic.

Working definitions from the notes:

- `basis` is a layer of reality beginning from the axiom that ideas are the fundamental substrate of our reality.
- `mediated.world` is the visualization of `basis`.
- A render translates data into an image.
- `mediated.world` cannot perfectly visualize `basis`; every render is a partial, situated attempt.
- The core axioms are:
  - ideas are the fundamental substrate of our reality;
  - information transfer is represented as light;
  - distance follows as idea relatedness.

Rendering rules:

- Visual effects must be generated from data: audio, track position, body masks, truck masks, camera motion, SLAM reconstruction, segmentation, or explicit idea mappings.
- Light should represent information transfer. It should not be arbitrary glow.
- Space should represent idea-space as much as physical space. SLAM geometry is useful when it helps physical travel become readable as movement through `mediated.world`.
- Effects need reasons inside the system. A blob, trail, field, or color shift should correspond to transmitted information, mediation, specificity, energy, relation, or motion.
- The body, truck, sky, road, and landscape can be treated as entities or surfaces that receive, block, emit, filter, or transform information.
- Avoid pure decoration unless it is explicitly framed as noise, uncertainty, or unmediated idea material.

Color and light rules:

- Hue maps to information content or mediation.
- Similar hues imply similar ideas.
- Complementary hues imply opposing ideas.
- Tertiary colors can imply support around a broader central idea.
- Saturation maps to specificity or complexity.
- Value maps to intensity, energy, or the pace of information transmission.
- White light can represent all information or an infinite/full information state.
- Iridescence can represent a spread of information that is nearly attainable but not fully captured.

Space and volume rules:

- Ideas can be represented as points, regions, or volumes in space.
- Density can represent how much thought or attention is concentrated on an idea.
- Dense idea regions should absorb or reduce passing light because information has been received or experienced there.
- Light sources can be ideas being actively shared.
- The unmediated center is an idea with no mediation and a lack of information; with no mediation, the render should tend toward idea material rather than literal imagery.

## Visual Effects Direction

- Use body segmentation to isolate the DJ/performance layer.
- Apply audio-reactive effects to the body mask.
- Explore effects that emit from the body, such as blobs, particles, trails, fields, or light forms.
- If possible, make emitted effects respond to the direction and movement of the drive.
- Segment or mask the truck so effects can interact with it, appear behind it, or be occluded by it.
- Segment sky, road, and background separately so each layer can receive independent color grading or treatment.
- Consider using SAM-2 body masking to make the performer less identifiable while keeping the performance readable.
- Consider AI stylization passes where they make the hour-long video more visually rich, as long as the world remains coherent.

## Music Mapping

The track list data includes start times plus `x`, `y`, and `z` values for each track. Those coordinates can be treated as an abstract map of the mix.

Possible mappings:

- Hue represents the current track or mediation state.
- Track transitions should be visually important and clearly captured.
- Small changes in the music over time can appear as noise, turbulence, or texture.
- Specificity can map to volume, frequency-spectrum fill, or how tightly an effect resolves.
- Similar songs can visually blend, while more distinct tracks can push the world into a different state.

## 3D Reconstruction Idea

Ideally, use SLAM or another camera-tracking/reconstruction workflow to map the drive into 3D space.

That would let visual effects interact with the world instead of only the screen plane. For example, blobs spawned from my body could drift backward in the same world direction as the moving truck, or particles could attach to reconstructed road, sky, and desert geometry.

## Potential Release Formats

- One-hour 2D video release.
- Short teaser clips for social release.
- 360/WebVR version synced with the mix in real time.
- Installation or live-show version.
- Multiplayer/world version if it becomes part of a larger Muse or mediated-world experience.

## Constraints

This is an offline render project. Real-time performance is not important.

Available hardware includes an NVIDIA RTX 3070 GPU. Overnight render times are acceptable if the result is meaningfully better.

## Current Files

- `firstpersontree.toe` - TouchDesigner project.
- `data/jtsm_tracks.csv` - track list data for the mix.
