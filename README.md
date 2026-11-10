# MID-3K — Raw LiDAR point clouds

[Main dataset repository](https://github.com/kennedyk1/MID-3K) · [Dataset website](https://kennedyk1.github.io/MID-3K/) · [Metadata](https://github.com/kennedyk1/MID-3K/blob/main/metainfo.csv)

This repository contains the raw LiDAR point clouds used to generate the depth and intensity modalities of the MID-3K Multimodal ISR Dataset.

## Repository contents

| Path | Format | Count | Description |
| --- | --- | ---: | --- |
| `pcd/` | Binary little-endian PLY | 3,083 | Point clouds associated with the MID-3K modalities |

All point-cloud stems match the 3,083 associated RGB, Thermal, Depth, and Intensity-label stems. Approximate data size: **6.5 GB**.

Each PLY vertex stores four `float` fields:

```text
x y z intensity
```

## LiDAR specification

| Field | Value |
| --- | --- |
| LiDAR | Ouster OS1-64-U |
| Vertical resolution | 64 channels |
| Horizontal resolution | 2,048 points per scan |

## Calibration

Use the canonical matrices from the main dataset repository according to the target camera:

- [COLOR camera from LiDAR](https://github.com/kennedyk1/MID-3K/blob/main/calibration/color_lidar/calibration.yaml)
- [THERMAL camera from LiDAR](https://github.com/kennedyk1/MID-3K/blob/main/calibration/thermal_lidar/calibration.yaml)

The transform direction and translation units are documented in the corresponding YAML files. Use [`metainfo.csv`](https://github.com/kennedyk1/MID-3K/blob/main/metainfo.csv) for scene metadata and reproducible associations.

## Related repositories

| Data | Repository |
| --- | --- |
| RGB images | [MID-3K-rgb](https://github.com/kennedyk1/MID-3K-rgb) |
| Thermal images | [MID-3K-thermal](https://github.com/kennedyk1/MID-3K-thermal) |
| Depth images | [MID-3K-depth](https://github.com/kennedyk1/MID-3K-depth) |
| Intensity images | [MID-3K-intensity](https://github.com/kennedyk1/MID-3K-intensity) |
