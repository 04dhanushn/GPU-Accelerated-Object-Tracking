# GPU-Accelerated Tracking of an Unregistered Object Across Video Frames

## Objective

Design and implement a GPU-accelerated object tracking system to track a single user-initialized object across video frames.

---

## System Modules

### 1. GPU-Accelerated Generic Object Tracker
Tracks the selected object in each frame without relying on predefined object classes.

### 2. Constant Velocity Motion Model
Predicts the target's next position assuming constant velocity.

### 3. Confidence Fusion
Combines tracker confidence and motion confidence to generate smooth and stable tracking.

---

## Inputs

- Video file (.mp4)
- Initial bounding box selected in first frame

---

## Outputs

For every frame:

- Bounding Box (x, y, width, height)
- Tracker Confidence
- Motion Model Confidence
- Trusted Output Source

Generated output files:

- tracked_video.mp4
- tracking_output.csv

---

## Architecture

Input Video

↓

Generic Object Tracker

+

Constant Velocity Motion Model

↓

Fusion Layer

↓

Tracked Video + CSV Output

---

## Build Instructions

Install dependencies:

```bash
pip install -r requirements.txt
```

Run:

```bash
jupyter notebook
```

Open:

```text
detection.ipynb
```

Execute all cells.

Select target object.

Wait until:

```text
Completed
```

---

## Dependencies

- OpenCV
- NumPy
- Pandas

---

## Repository Structure

```text
input/
output/
docs/
README.md
requirements.txt
LICENSE
detection.ipynb
```
