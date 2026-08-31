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

## 사사
본 연구는 과학기술정보통신부 및 정보통신기획평가원의 자율주행기술개발혁신사업의 지원을 받아 수행된 연구임 (RS-2023-00232046, 비정상 주행 데이터 전송을 통한 클라우드 기반 원인 분석 기술 개발).

This work was partly supported by Institute of Information & communications Technology Planning & Evaluation (IITP) grant funded by the Korea government(MSIT) (No.2023-00232046, Development of cloud-based cause analysis technology by transmission of abnormal driving data)
