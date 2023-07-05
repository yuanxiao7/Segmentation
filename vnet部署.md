vnet部署

```python
E:\DL_environments\SoftwareSegmentation\Segmentation\PaddleSeg\contrib\MedicalSeg  下的export.py运行命令

 python export.py --config E:/DL_environments/SoftwareSegmentation/Segmentation/test_configs/vnet_e
xample.yml --model_path E:/DL_environments/SoftwareSegmentation/Segmentation/baseline_model/best_model/model.pdparams --save_dir E:/DL_environments/SoftwareSegmentation/Segmentation/ba
seline_model/vnet/export_model
```

遇到如下报错，并得到解决

```python
 print(imgs_path)

['data/competition_raw/competition_dataset/imagesTs\\07abcf87-8ec7-4d31-9ee5-7a604894a913.nii.gz', 'data/competition_raw/competition_dataset/imagesTs\\07abcf87-8ec7-4d31-9ee5-7a604894a913.npy', 
此处省略40多组
···

'data/competition_raw/competition_dataset/imagesTs\\f8d197fc-b6f0-4b1e-adc3-ba3f373dcaf3.nii.gz', 'data/competition_raw/competition_dataset/imagesTs\\f8d197fc-b6f0-4b1e-adc3-ba3f373dcaf3.npy']

FileNotFoundError: [Errno 2] No such file or directory: 'data/competition_raw/competition_dataset/imagesTs\\imagesTs\\07abcf87-8ec7-4d31-9ee5-7a604894a913.npy'

img：
E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs\07abcf87-8ec7-4d31-9ee5-7a604894a913.nii.gz

去掉后缀的img
E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs\imagesTs\07abcf87-8ec7-4d31-9ee5-7a604894a913
```

找到路径切错的代码，然后改回来，错因：win的路径斜杠和反斜杠符号不同作用同，用sblit()时路径出错



上述问题解决后，运行出现一下问题

这个是因为设置使用显卡，但是跑的时候没有使用显卡而触发的报错，改成gpu就好了

![image-20230704222610588](E:\picture\软件杯\error1.png)

解决完以后，又遇到了

```
Exception thrown in SimpleITK ImageFileReader_Execute: D:\a\1\sitk\Code\IO\src\sitkImageReaderBase.cxx:105:
E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs\imagesTs\07abcf87-8ec7-4d31-9ee5-7a604894a913
```

这个是路径中的斜杠和反斜杠导致的，把斜杠调成反斜杠即可

及接着就遇到一下报错,因为推理之前需要删除文件夹下的所有.npy文件

```
 Unable to determine ImageIO reader for "E:/DL_environments/SoftwareSegmentation/Segmentation/PaddleSeg/contrib/MedicalSeg/data/competition_raw/competition_dataset/imagesTs/07abcf87-8ec7-4d31-9ee5-7a604894a913.npy"
```

终于，成功推理

不过，存在文件不能全部推理的问题，只有12个成功推理，然后我又重新预处理数据，时而给出现电脑win不支持什么的弹窗。后面直接是只能推理一两个，把我整蒙了，吐血，于是我决定让电脑休息一会，关机，重新开机。重新运行，这回完整的正常推理 。

