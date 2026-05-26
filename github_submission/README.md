# D-RTMDet Supplementary Materials

This repository contains the public supplementary materials for the manuscript:

**D-RTMDet: A Depth-Prior-Guided Lightweight Model for Paddy Headland Segmentation Using RGB-Only Inference**

## Contents

| Path | Description |
| --- | --- |
| `weights/epoch_160.pth` | Trained checkpoint specified for submission. |
| `test_data/val2017/` | Seven RGB test images. |
| `test_data/annotations/instances_refined_val2017_7.json` | COCO-format annotation file for the seven test images. |
| `pseudocode/D-RTMDet_pseudocode.tex` | LaTeX pseudocode for the D-RTMDet training and RGB-only inference procedures. |
| `SHA256SUMS.txt` | SHA256 checksums for all provided files. |

## Test Data

The test subset contains seven RGB images:

`0015.jpg`, `0125.jpg`, `0364.jpg`, `0466.jpg`, `0523.jpg`, `0524.jpg`, and `0809.jpg`.

The annotation file uses COCO format and contains one category:

```json
{"id": 1, "name": "tiantou"}
```

## Model Weight

The checkpoint is:

`weights/epoch_160.pth`

File size: `169,642,867` bytes.

SHA256:

```text
A836B426341081ED77B388A82650D074BCA69DB9D8FAA096788056E5FB7C7335
```

Because this file is larger than GitHub's 100 MB regular file limit, the repository is prepared for **Git LFS** via `.gitattributes`. Alternatively, upload the checkpoint as a GitHub Release asset and link it from this README.

## Pseudocode

The pseudocode file contains two algorithms:

1. Training procedure of D-RTMDet.
2. Inference procedure of D-RTMDet.

The inference procedure uses RGB input only.

## Integrity Check

After downloading the repository, verify file integrity with SHA256 checksums:

```powershell
Get-FileHash -Algorithm SHA256 weights\epoch_160.pth
```

The expected hashes for all files are listed in `SHA256SUMS.txt`.
