# SNU_LAAL_PCDetection
## Data Preparation
We use **OpenPCDet**, an open-source toolbox for LiDAR-based 3D object detection ([OpenPCDet GitHub Repository](https://github.com/open-mmlab/OpenPCDet)), to process the **KITTI 3D Object Detection Dataset** ([KITTI Dataset Information](https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d)).
Refer to the [Getting Started Guide](https://github.com/open-mmlab/OpenPCDet/blob/master/docs/GETTING_STARTED.md) of the **OpenPCDet** library to properly organize the **KITTI dataset**. Once the dataset is organized correctly, run the following command to preprocess the data:

```bash
python -m pcdet.datasets.kitti.kitti_dataset create_kitti_infos tools/cfgs/dataset_configs/kitti_dataset.yaml
```
Once preprocessing is complete, you can easily use the dataloader by importing the following function:

```python
from pcdet.datasets import build_dataloader
```