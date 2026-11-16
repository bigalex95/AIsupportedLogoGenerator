# AIsupportedLogoGenerator

University experiments (2021) in generating logo images with GANs: DCGAN and WGAN notebooks plus a StyleGAN2 Colab notebook, trained on logo datasets. There is no web app and no text/keyword conditioning here. Not maintained.

## What's inside

```
Code/
  dcgan/dcgan.py, wgan/wgan.py        PyTorch DCGAN / WGAN scripts (from eriklindernoren/PyTorch-GAN)
  jupyter_notebooks/
    eriklindernoren_PyTorch-DCGAN.ipynb
    eriklindernoren_Pytorch-WGAN.ipynb
    config-f StyleGAN2 Google Colab v2     StyleGAN2 (config-f) training notebook, Colab; file has no .ipynb extension
  preprocessing/
    data_prep.py     crop OpenLogo images to their bounding boxes
    crop_image.py    resize images (128 px, Colab/Drive paths hard-coded)
    scale.py         resize images to 400x400
Database/Database.txt   Links to the datasets used (QMUL-OpenLogo, LLD)
```

## Run

Not packaged: there is no requirements file, and the preprocessing scripts contain hard-coded paths (`./train/`, `/content/drive/MyDrive/...`) that you need to edit.

1. Download a dataset from the links in `Database/Database.txt`.
2. Crop and resize with the scripts in `Code/preprocessing/`.
3. Train in the notebooks, ideally on Colab with a GPU (the StyleGAN2 notebook uses TensorFlow 1.x and clones NVlabs/stylegan2).

The old README also told you to clone `ConditionalStyleGAN` and `stylegan-web`. I never included those, and they are not part of this repo. I did not re-run any of this.

## Results

No generated samples or metrics are committed. The original Turkish project report (PDF) was removed from the repo to keep it small.

## Status

2021 coursework experiment, not maintained.

## Credits

- [eriklindernoren/PyTorch-GAN](https://github.com/eriklindernoren/PyTorch-GAN): DCGAN and WGAN code.
- [NVlabs/stylegan2](https://github.com/NVlabs/stylegan2): StyleGAN2 (cloned by the Colab notebook).
- [cedricoeldorf/ConditionalStyleGAN](https://github.com/cedricoeldorf/ConditionalStyleGAN) and [k-l-lambda/stylegan-web](https://github.com/k-l-lambda/stylegan-web): referenced by the original instructions, not included.
- Datasets: QMUL-OpenLogo and LLD (Large Logo Dataset), see `Database/Database.txt`.
