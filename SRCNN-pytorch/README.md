# SRCNN

This repository is implementation of the ["Image Super-Resolution Using Deep Convolutional Networks"](https://arxiv.org/abs/1501.00092).


## Requirements

- PyTorch 1.0.0
- Numpy 1.15.4
- Pillow 5.4.1
- h5py 2.8.0
- tqdm 4.30.0

## Train

- Selecting and download dataset we provid: [91-image](https://drive.google.com/drive/folders/1DlDbMYjYk9K2Z-Or83kSloDZZAcmVTQF?usp=share_link), [Set5](https://drive.google.com/drive/folders/1QAAYUWV4p4DiHynXxhxy5fHESYpsninY?usp=share_link), or [Urban-100](https://drive.google.com/drive/folders/1-32AkTyJoj-k5Dlx5SKmfJfCYbBMOK75?usp=share_link)

- Otherwise, you can use `prepare.py` to create custom dataset by convering to HDF5.

### How to run

```
python train.py --train-file "BLAH_BLAH/urban100_x2.h5" \
                --eval-file "BLAH_BLAH/Set5_x2.h5" \
                --outputs-dir "BLAH_BLAH/outputs" \
                --scale 2 \
                --lr 1e-4 \
                --batch-size 16 \
                --num-epochs 20 \
                --num-workers 8 \
                --seed 123                
```



## Test

- Find the weights file under `BLAH_BLAH/output/x2/best_psnr.pth`
- Test by applying your own image and to see the result

### How to run
```
python test.py --weights-file "BLAH_BLAH/output/x2/best_psnr.pth" \
               --image-file "data/your_image.bmp" \
               --scale 2
```

## Result
- Test result by pretained model 
  - [Original Pictures](https://drive.google.com/drive/folders/16FY-BWGAb0JktlzPfVgXWczCE75UkT09?usp=share_link)
  - [weights file](https://drive.google.com/drive/folders/1EpMve4jHRMc7HlMOghnioL8Q2sT1qBjr?usp=share_link)
  - [Image Test Result](https://drive.google.com/drive/folders/1nF6Q-OQb5nlqYLWZ_OJW5NnoGQph-Qb_?usp=share_link)

