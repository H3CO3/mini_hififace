# Face swapping to painting

Adapt from [hififace](https://github.com/mindslab-ai/hififace) and [MSG-Net](https://github.com/zhanghang1989/PyTorch-Multi-Style-Transfer)
Code test in Windows. Requirement to be added later.

### Download pre-trained Model:
Please download [hififace_opensouce_299999.ckpt](https://drive.google.com/file/d/1tZitaNRDaIDK1MPOaQJJn5CivnEIKMnB/view?usp=sharing) and [ms1mv3_arcface_r100_fp16_backbone.pth](https://1drv.ms/u/s!AswpsDO2toNKq0lWY69vN58GR6mw?e=p9Ov5d)  and store in this floder
```bash
## download bash to be added later
```
And also download model in `model/README.md` and `model/Deep3DFaceRecon_pytorch/README.md`


### Swapping face:
Swap the face in `source_image_path` to `target_image_path`.
```bash
python hififace_inference.py --gpus 0 --model_config config/model.yaml --model_checkpoint_path hififace_opensouce_299999.ckpt \
--output_image_path assets/result/swap_result.png \
--source_image_path assets/inference_samples/03_target.png \
--target_image_path assets/AF_dataset/Pablo_Picasso/111.png
```
Swap faces: Code to be added later

### Style Transfer:
Transfer picture to `--style-imag` style.
```bash
python MSG_main.py eval --content-image assets/result/result.png \ 
--style-image assets/21styles/picasso_selfport1907.jpg --model models/21styles.model --content-size 256 \
--output-image assets/result/transfer_result.png
```
Pre-trained style stored in `assets/21styles` \
More pre-trained (on our dataset) to be added later



