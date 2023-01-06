# Finetuning CLIP with huggingface libs

This notebook demonstrates how to finetune the type of CLIP models used for Stable Diffusion with huggingface libs on a self-defined dataset. 

Based on [the huggingface transformers CLIP example](https://github.com/huggingface/transformers/tree/main/examples/pytorch/contrastive-image-text).

## Dataset

The dataset should be provided as a collection of images as `.jpg` or `.jpeg` files. For each file, there should be a `.txt` file with the same name that contains the caption:

* `fluffy-dog.jpg` 
* `fluffy-dog.txt` - caption for `fluffy-dog.jpg`, for example `a picture of a fluffy dog`.

In the `huggingface_finetune_clip_runner.ipynb` is a code cell that outputs a `.json` file in a format that huggingface datasets can understand for such a collection of files. 

## Finetuning

Load `huggingface_finetune_clip_runner.ipynb` in an environment that already has PyTorch and torchvision installed. Work through the cells one by one - you will need to change the `root_folder` and `out_json` to match your needs:

```
root_folder = "/Users/damian/2.current/stablediffusion/buzzybee/fullsize"
out_json = "/Users/damian/2.current/stablediffusion/buzzybee.json"
```

