# URsNet
URsNet: Unsupervised Remote Sensing Stitching Network for low-altitude UAV Images


## 1. Evaluation Setting

| Item | Setting |
|---|---|
| Input size | 512 x 512 image pair |
| GPU | NVIDIA RTX 3090 |
| Measurement protocol | Average inference time after model warm-up |
| Task | Pairwise UAV image stitching |

## 2. Inference Speed

For a pair of 512 x 512 images, URsNet takes:

| Metric | Value |
|---|---:|
| Inference time | 0.134 s / pair |
| Throughput | 7.43 FPS |

This speed can match the image acquisition rhythm of many UAV aerial mapping scenarios where images are captured at intervals. Here, near-real-time refers to matching the acquisition pace of UAV image collection, not video-level frame-by-frame stitching at 25-30 FPS.

## 3. Model Complexity

| Module | Parameters | GMACs | GFLOPs |
|---|---:|---:|---:|
| Registration module | 127.19 M | 69.1 | 138.2 |
| Fusion module | 9.29 M | 62.4 | 124.8 |
| Full model | 136.5 M | 131.5 | 263.0 |
