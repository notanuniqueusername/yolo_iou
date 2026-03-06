# Video Object Detection with YOLO11n

> Single-object detection on video using YOLO11n, evaluated against manual ground truth annotations via IoU.

---

## Experiment Setup

| Parameter | Value |
|---|---|
| Model | YOLO11n (pretrained) |
| Input | test.mp4 |
| Confidence Threshold | 0.4 |
| Evaluation Metric | Intersection over Union (IoU) |
| Annotated Frames | 3 |

---

## Ground Truth Annotations

| Frame | Bounding Box (x1, y1, x2, y2) |
|:---:|---|
| 50 | [1287, 279, 1631, 893] |
| 120 | [756, 234, 1252, 900] |
| 200 | [636, 190, 1230, 910] |

---

## IoU Results

| Frame | IoU Score |
|:---:|:---:|
| 50 | 0.9692 |
| 120 | 0.9503 |
| 200 | 0.9734 |
| **Average** | **0.9643** |

---

## Possible Improvements

- **Lower confidence threshold** — Reduce to 0.3 to catch edge cases with lower certainty
- **Upgrade model** — Switch to YOLO11s or YOLO11m for better accuracy at the cost of speed

---

## Conclusion

YOLO11n achieved **96.43% average IoU** across all annotated frames with consistent performance and zero false negatives. The model proved effective for real-time video object detection with minimal configuration.
