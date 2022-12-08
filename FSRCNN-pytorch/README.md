# FSRCNN

This repository is implementation of the ["Accelerating the Super-Resolution Convolutional Neural Network"](https://arxiv.org/abs/1608.00367).


## Requirements

- PyTorch 1.0.0
- Numpy 1.15.4
- Pillow 5.4.1
- h5py 2.8.0
- tqdm 4.30.0

## Train

- Selecting and download dataset we provid: [91-image](https://drive.google.com/drive/folders/1DlDbMYjYk9K2Z-Or83kSloDZZAcmVTQF?usp=share_link), Urban-100](https://drive.google.com/drive/folders/1-32AkTyJoj-k5Dlx5SKmfJfCYbBMOK75?usp=share_link), [Set5](https://drive.google.com/drive/folders/1QAAYUWV4p4DiHynXxhxy5fHESYpsninY?usp=share_link), [Set14](https://drive.google.com/drive/folders/18RqvSzVw_HBsh3ItdZG4Lq89Wc9HqkKc?usp=share_link), and [BSD100](https://drive.google.com/drive/folders/1doqVGCUc8_I1ylM65gKyl9WmMyWc2yrS?usp=share_link).

- Otherwise, you can use `prepare.py` to create custom dataset by convering to HDF5.

### How to run

```
python train.py --train-file "FSRCNN/urban100_x2.h5" \
                --eval-file "FSRCNN/Set5_x2.h5" \
                --outputs-dir "FSRCNN/outputs" \
                --scale 2 \
                --lr 1e-4 \
                --batch-size 16 \
                --num-epochs 100 \
                --num-workers 8 \
                --seed 123                
```

## Test

- Find the weights file under `FSRCNN/output/x2/best_psnr.pth`
- Test by applying your own image and to see the result

### How to run
```
python test.py --weights-file "FSRCNN/output/x2/best_psnr.pth" \
               --image-file "data/your_image.bmp" \
               --scale 2
```
## Result
- Test result by pretained model 
  - [Original Pictures](https://drive.google.com/drive/folders/1yT8jEDv_8SYn_BEQOdhrnbx5MbM2MIvu?usp=share_link)
  - [Image Test Result](https://drive.google.com/drive/folders/1l7Ngh76bdSdkW2_PBXBLylbhLFdj_CX3?usp=share_link)

