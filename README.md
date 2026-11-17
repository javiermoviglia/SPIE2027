# SPIE 2027 — Markerless augmented reality

Markerless AR demonstration for the paper **A Modular Registration Platform for Image-Guided Interventions**.

Live: https://javiermoviglia.github.io/SPIE2027/

## Visitor workflow

1. Open the poster QR link on an AR-compatible iPhone or Android smartphone.
2. Choose **NDI Polaris** or **Monocular NIR** in the web UI.
3. Select **View in AR**. A native viewer opens if supported.
4. Slowly scan the table or floor, place the model, and physically move closer or around it.
5. To switch trackers, return to the web page, select the other configuration, and enter AR again.

No poster image target or MindAR library is needed in main.

## Technical implementation

- Google model-viewer 4.3.0 through jsDelivr.
- Self-contained GLB models, with geometry in meters.
- Android: Scene Viewer or WebXR on a supported ARCore device.
- iPhone Safari: AR Quick Look using a USDZ generated on demand by model-viewer from the selected static GLB.
- The native AR view does not retain the website's HTML configuration buttons; select the tracker first.
- If AR is unsupported, the 3D viewer remains available in the webpage.
- Requires HTTPS, provided by GitHub Pages.

## Files

- index.html: responsive viewer, two tracker options, native AR launch.
- models/ndi-polaris.glb: illustration of NDI Polaris and shared navigation hardware.
- models/monocular-nir.glb: illustration of monocular NIR/ArUco and the same shared hardware.
- mindAR branch: full backup of the former image-target tracking implementation.

These GLB files are **conceptual 3D reconstructions** rather than engineering CAD, measured geometry, or real software screens. They illustrate modular reconfiguration and are not validated clinical navigation data.

## Device verification checklist

- [ ] Open models and switch configurations in Safari on a real iPhone.
- [ ] Place both variants in iOS Quick Look on an ARKit-compatible iPhone.
- [ ] Place both variants through Android Scene Viewer on a compatible ARCore phone.
- [ ] Move physically closer to the phantom to confirm device-based positional tracking.
- [ ] Ensure the model height/scale looks appropriate on a table and on the floor.
- [ ] Check QR points to GitHub Pages and not the previous target-tracking page.

Reference: https://modelviewer.dev/docs/index.html
