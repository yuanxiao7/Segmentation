V-Net推理

使用argparse模块

加有 config   image_path   batchz_size   save_dir   device  use_trt   precision  enable_auto_tune   auto_tuned_shape_file   cpu_threads   enable_mkldnn    benchmark   model_name   with_argmax   print_detail     use_swl     img_shape  is_nhwd

class Predictor 预测

run方法中传的是 

```
['E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs\\07abcf87-8ec7-4d31-9ee5-7a604894a913.nii.gz', 
```



```
              'E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/0f593c1e-4bb8-470f-a87b-fee3dbd3b3ed.nii.gz', 
              'E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/12dc6a4c-ba92-4ffb-98e3-dbd0827e8b8a.nii.gz', 
              'E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/1b08207d-fe04-4000-a813-840f8d0d2b7d.nii.gz',
              'E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/1e2dc581-e1c3-4492-aca7-ac0ae22eadb6.nii.gz',
              'E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/219a9c52-af31-400f-b693-0946835c8265.nii.gz', 
              'E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/27759b18-fd84-4798-b31d-4f23ed803d23.nii.gz'
```

