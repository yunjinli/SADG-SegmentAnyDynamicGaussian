# Dataset Preparation

## Download and Process the Dataset

### NeRF-DS

```
cd data/NeRF-DS
bash download_dataset.bash
```

For generating the anything-masks from SAM.

```
python extract_masks.py --img_path data/NeRF-DS/<NAME>/rgb/2x --output data/NeRF-DS/<NAME> --iou_th 0.88 --stability_score_th 0.95 --downsample_mask 2
```

### HyperNeRF

```
cd data/HyperNeRF
bash download_dataset.bash
```

For generating the anything-masks from SAM.

```
python extract_masks.py --img_path data/HyperNeRF/<interp/misc>/<NAME>/rgb/2x --output data/NeRF-DS/<NAME> --iou_th 0.88 --stability_score_th 0.95 --downsample_mask 2
```

### Neu3D

```
cd data/Neu3D
bash download_dataset.bash
```

For generating initial point cloud. Make sure you have COLMAP installed. We use COLMAP 3.9.1.

```
python neu3d2blender.py --path data/Neu3D/<NAME> --scale 2
```

For generating the anything-masks from SAM.

```
python extract_masks.py --img_path data/Neu3D/<NAME>/images_2x --output data/Neu3D/<NAME> --iou_th 0.88 --stability_score_th 0.95 --downsample_mask 4
```

### Google Immersive

Download the dataset from [here](https://github.com/augmentedperception/deepview_video_dataset). Note that we only use 01_Welder, 02_Flames, 10_Alexa_Meade_Face_Paint_1, and 11_Alexa_Meade_Face_Paint_2.

For generating initial point cloud. Make sure you have COLMAP installed. We use COLMAP 3.9.1.

```
python immersive2blender.py --path data/immersive/<NAME> --scale 2 --end 50
```

For generating the anything-masks from SAM.

```
python extract_masks.py --img_path data/immersive/<NAME>/images_2x --output data/immersive/<NAME> --iou_th 0.88 --stability_score_th 0.95 --downsample_mask 4
```

### Technicolor Light Field

Please contact the author from "Dataset and Pipeline for Multi-View Light-Field Video" for access. We use the undistorted data from Birthday, Fabien, Painter, and Theater.

For generating initial point cloud. Make sure you have COLMAP installed. We use COLMAP 3.9.1.

```
python technocolor2blender.py --path data/technicolor/Undistorted/<NAME> --scale 2
```

For generating the anything-masks from SAM.

```
python extract_masks.py --img_path data/technicolor/Undistorted/<NAME>/images_2x --output data/technicolor/Undistorted/<NAME> --iou_th 0.88 --stability_score_th 0.95 --downsample_mask 2
```