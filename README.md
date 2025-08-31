1. score_threshold

This controls minimum confidence for a detection to be considered valid.

Each predicted bounding box has a confidence score (e.g., 0.92 = 92% sure it’s a car).

👉 What happens if you change it:

Increase it (e.g., 0.5 → 0.8):

Model will keep only very confident predictions.

Fewer boxes shown → lower recall, higher precision.

Might miss some cars if model isn’t very confident.

Decrease it (e.g., 0.5 → 0.2):

Model will show more boxes, including low-confidence ones.

More detections → higher recall, lower precision.

May add false positives (detects a “car” where there isn’t one).

🔹 2. iou_threshold

IoU = Overlap ratio between two bounding boxes.

Used during NMS (Non-Maximum Suppression) to remove duplicate boxes for the same object.

👉 What happens if you change it:

Increase it (e.g., 0.5 → 0.8):

Model will allow boxes to overlap more before suppressing.

You may see duplicate detections for the same car (multiple boxes on one car).

Decrease it (e.g., 0.5 → 0.2):

Model will aggressively suppress overlapping boxes.

Fewer duplicates, but might remove true positives if two cars are very close together.
