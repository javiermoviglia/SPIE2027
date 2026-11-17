# SPIE 2027: One workflow, two trackers

Single-image-target WebAR demonstration of the modular registration platform.

**Fig. 1** (the graph-based platform image) is the only image target. Two phone buttons alternate **NDI Polaris** and **Monocular NIR / ArUco**. Each view places a conceptual software-graph screen next to a simplified setup: gelatin phantom, tracked ultrasound probe, needle, projector guidance and the selected optical tracker.

The tracker and marker type change; the ultrasound-guided navigation workflow remains the same.

These are illustrative conceptual graphics, not actual software screenshots or CAD models. This is an explanation of workflow reconfiguration rather than accuracy measurement.

## Required target files

The web code is included, but camera-based recognition needs two binary assets added to the repository:

1. Upload the user's exact Fig. 1 image as **fig1.jpg** to the repository root.
2. Open https://hiukim.github.io/mind-ar-js-doc/tools/compile/ and compile only this image.
3. Download the file, rename it **fig1.mind**, and upload it to the repository root.
4. Merge the feature branch to main; open https://javiermoviglia.github.io/SPIE2027/ on an HTTPS-enabled phone and scan Fig. 1.

Do not compile the entire poster or substitute a different crop. Print matte and large enough for stable tracking.

## Test and preview

- AR page: https://javiermoviglia.github.io/SPIE2027/
- Fig. 1 instructions: https://javiermoviglia.github.io/SPIE2027/target.html
- **2D-only preview:** https://javiermoviglia.github.io/SPIE2027/?preview=1
- One image target, index 0. No external example targets.
- Test camera recognition, both switch buttons, reacquisition, iOS Safari and Android Chrome before the conference.

Stack: A-Frame 1.5.0 and MindAR 1.2.5.
