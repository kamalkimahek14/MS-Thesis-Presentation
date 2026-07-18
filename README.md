# Thesis Defense Presentation — Object Classification, Detection and State Estimation using YOLO-v3 and Sensor Fusion of Stereo Camera and LiDAR

LaTeX Beamer slide deck for the Master's thesis defense of **Kamalkumar Mehta** (Aerospace System Laboratory, Department of Mechanical and Aerospace Engineering, The University of Texas at Arlington), supervised by Dr. Kamesh Subbarao. Presented June 2021.

This is the **full-length version** of the defense deck (~68 frames). A condensed version lives in `../Thesis-presentation-Updated`.

## Contents of the Talk

The deck covers the complete thesis pipeline for real-time object detection and state estimation on an autonomous ground vehicle:

1. **Motivation & Background** — real-time detection for ADAS/collision avoidance; comparison with R-CNN family.
2. **YOLO-v3 Architecture** — network layers, activation functions, convolution operations.
3. **Data Preprocessing** — dataset creation, labeling, and augmentation.
4. **Supervised Learning** — transfer learning on a custom four-shape dataset.
5. **Hyper-parameters Tuning** — mini-batch size, L2 regularization, epochs, learning rate.
6. **YOLO Algorithm** — anchor boxes, IoU, loss function.
7. **Training & Testing Results** — loss/precision plots, confusion chart, detection examples.
8. **Optical Sensor & Calibration** — intrinsic/extrinsic calibration of stereo camera (Sony IMX 179) and Intel RealSense L515 LiDAR.
9. **Sensor Fusion** — centralized fusion framework with a linear Kalman filter.
10. **Simulation & Experimental Results** — MATLAB Driving Scenario simulation and hardware experiments.
11. **Conclusion & Future Work**

## Repository Structure

| Path | Description |
|---|---|
| `main.tex` | The full Beamer deck (Madrid theme, UTA colors) — compile this file. |
| `ref.bib` | Bibliography for cited works (biblatex). |
| `UTA.png` | UTA logo shown on each slide. |
| `Images/` | All slide figures: network diagrams, calibration figures, training plots, and experiment screenshots. |

## Building

Requires a LaTeX distribution with Beamer and biblatex (biber backend):

```
pdflatex main.tex
biber main
pdflatex main.tex
```

The output is `main.pdf`.

## Related Projects

- `../Thesis_report` — the full thesis document these slides summarize.
- `../Thesis-presentation-Updated` — condensed version of this deck.
