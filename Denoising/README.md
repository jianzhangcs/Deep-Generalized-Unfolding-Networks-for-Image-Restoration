## Training
- Download the [Datasets](Datasets/README.md)

- Generate image patches from full-resolution training images of SIDD dataset
```
python generate_patches_SIDD.py --ps 256 --num_patches 300 --num_cores 10
```
- Train the model with default arguments by running

```
python train.py
python train_plus.py
```


## Evaluation

- Download the [model](https://drive.google.com/file/d/1bitvtmJAE1iKpFmdGx3OrN6Xti0JRPLc/view?usp=sharing) and place it in `./pretrained_models/`

#### Testing on SIDD dataset
- Download SIDD Validation Data and Ground Truth from [here](https://www.eecs.yorku.ca/~kamel/sidd/benchmark.php) and place them in `./Datasets/SIDD/test/`
- Run
```
python test.py --save_images
python test_plus.py --save_images
```

#### To reproduce PSNR/SSIM scores of the paper, run MATLAB script
```
evaluate_SIDD.m
```
