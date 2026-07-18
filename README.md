# Thesis Defense Presentation (Updated / Condensed) — Object Classification, Detection and State Estimation using YOLO-v3 and Sensor Fusion of Stereo Camera and LiDAR

Condensed LaTeX Beamer slide deck for the Master's thesis defense of **Kamalkumar Mehta** (Aerospace System Laboratory, Department of Mechanical and Aerospace Engineering, The University of Texas at Arlington), supervised by Dr. Kamesh Subbarao. Presented June 2021.

This is a **shortened revision** of `../Thesis_presentation` (~48 frames vs. ~68): the standalone *Data Preprocessing* and *Testing Results* sections were removed and other material tightened, making it better suited to a time-limited talk.

## Contents of the Talk

1. **Motivation & Background** — real-time detection for ADAS/collision avoidance; comparison with the R-CNN family.
2. **YOLO-v3 Architecture** — network layers, activation functions, convolution operations.
3. **Supervised Learning** — transfer learning on a custom four-shape dataset (cylinder, cone, pyramid, box).
4. **Hyper-parameters Tuning** — mini-batch size, L2 regularization, epochs, learning rate.
5. **YOLO Algorithm** — anchor boxes, IoU, loss function.
6. **Training Results** — loss/precision plots and detection examples.
7. **Optical Sensor & Calibration** — intrinsic/extrinsic calibration of stereo camera (Sony IMX 179) and Intel RealSense L515 LiDAR.
8. **Sensor Fusion** — centralized fusion framework with a linear Kalman filter.
9. **Simulation & Experimental Results** — MATLAB Driving Scenario simulation and hardware experiments.
10. **Conclusion & Future Work**

## Repository Structure

| Path | Description |
|---|---|
| `main.tex` | The condensed Beamer deck (Madrid theme, UTA colors) — compile this file. |
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
- `../Thesis_presentation` — the original full-length defense deck.
