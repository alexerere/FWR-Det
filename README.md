# FWR-Det

## Download

- [Download FWR-Det from Baidu Netdisk](https://pan.baidu.com/s/1hx9EG1PcTIEW3zdF7diitw)
- Access code: gsrh

FWR-Det is a ground-view image dataset for fixed-wing unmanned aerial vehicle detection in vision-assisted recovery. The dataset contains 11361 RGB images and 11490 bounding-box annotations for a single UAV class. Images were extracted from 113 video clips, with each clip assigned to one subset.

Project repository: <https://github.com/alexerere/FWR-Det>

## Dataset version and splits

The dataset version is **FWR-DET**. The predefined training, validation and test splits are:

| Subset | Images | Bounding boxes | Source clips |
| --- | ---: | ---: | ---: |
| Training | 7964 | 8093 | 75 |
| Validation | 1123 | 1123 | 11 |
| Test | 2274 | 2274 | 27 |
| Total | 11361 | 11490 | 113 |

## Dataset organisation

The image-label dataset uses the following directory structure:

```text
FWR-DET/
├── images/
│   ├── train/
│   ├── val/
│   └── test/
├── labels/
│   ├── train/
│   ├── val/
│   └── test/
└── data.yaml
```

An image and its label file share the same filename stem. Clip identifiers link related images to their source clip and assigned subset.

## Annotation format

Annotations use the YOLO text format, with one bounding box per line:

```text
class_id x_center y_center width height
```

The class identifier is `0` for `UAV`. Centre coordinates and box dimensions are normalised by the original image width and height.

## Dataset configuration

The configuration example in `data.yaml` defines the single class and the three image subsets. Set `path` to the absolute location of the downloaded `FWR-DET` directory before using it with a compatible detector implementation. Keep the predefined splits for comparison with the manuscript results.

## Authors and contact

Yu Yao, Jun Wu, Jun Zhu and Yisheng Hao

College of Intelligence Science and Technology, National University of Defense Technology, Changsha 410073, China

Corresponding author: Jun Wu — <wujun2008@nudt.edu.cn>
