# mini_hififace

Adapt from [hififace](https://github.com/mindslab-ai/hififace) and [MSG-Net](https://github.com/zhanghang1989/PyTorch-Multi-Style-Transfer)

### Swapping face:
Swap the face in `source_image_path` to `target_image_path`
```bash
python hififace_inference.py --gpus 0 --model_config config/model.yaml --model_checkpoint_path hififace_opensouce_299999.ckpt \
--output_image_path assets/result/result.png \
--source_image_path assets/AF_dataset/Raphael/source.png \
--target_image_path assets/AF_dataset/Raphael/120.png
```


Style Transfer:




Download pre-trained Model:
Please download [hififace_opensouce_299999.ckpt](https://drive.google.com/file/d/1tZitaNRDaIDK1MPOaQJJn5CivnEIKMnB/view?usp=sharing) and [ms1mv3_arcface_r100_fp16_backbone.pth](https://1drv.ms/u/s!AswpsDO2toNKq0lWY69vN58GR6mw?e=p9Ov5d)  and store in this floder

And download model setting in model/Deep3DFaceRecon_pytorch/readme.md
