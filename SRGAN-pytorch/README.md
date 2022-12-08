# SRGAN

This repository is implementation of the ["Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network"](https://arxiv.org/abs/1609.04802).


## Requirements

- PyTorch 
- numpy
- pandas
- matplotlib
- h5py
- tqdm

## Train
- Selecting and download dataset we provid: [91-image](https://drive.google.com/drive/folders/1DlDbMYjYk9K2Z-Or83kSloDZZAcmVTQF?usp=share_link), [Urban-100](https://drive.google.com/drive/folders/1-32AkTyJoj-k5Dlx5SKmfJfCYbBMOK75?usp=share_link), [Set5](https://drive.google.com/drive/folders/1QAAYUWV4p4DiHynXxhxy5fHESYpsninY?usp=share_link), [Set14](https://drive.google.com/drive/folders/18RqvSzVw_HBsh3ItdZG4Lq89Wc9HqkKc?usp=share_link), and [BSD100](https://drive.google.com/drive/folders/1doqVGCUc8_I1ylM65gKyl9WmMyWc2yrS?usp=share_link).

- Put your images into folder `train`, `valid`, `test` folder in folder `data`.

### How to run

```
python train.py \

optional arguments:
--crop_size                   training images crop size\
--upscale_factor              super resolution upscale factor\
--num_epochs                  the number of trainning epoch\
```


## Test

- Put your test image in the `test` folder, and test by applying your own image and to see the result.

### How to run
```
python test_image.py --image_name="image_name.png" --model_path="best_SRGAN.pth"

optional arguments:\
--upscale_factor              super resolution upscale factor \
--test_mode                   using GPU or CPU \
```

## Result
- Test result by pretained model 
  - [Original Pictures](https://drive.google.com/drive/folders/1S8aXek99FzXTc7HEMqR341ID2Uubxm_Y?usp=share_link)
  - [Image Test Result](https://drive.google.com/drive/folders/1QvDoP-U7Ux3CxgY_flRnxA4lqsDX9BD8?usp=share_link)


