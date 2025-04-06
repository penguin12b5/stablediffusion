## My Notes

### Script arguments
```
--prompt "summer time at beach" 
--ckpt checkpoints/v2-1_768-ema-pruned.ckpt 
--config configs/stable-diffusion/v2-inference-v.yaml 
--device cuda

--n_samples: size of batch or how many picture to generate for each row, eg. 1
--n_iter: how often to sample, default to 3. set to 1 for 1 picture 
(so total pictures to generate is n_samples * n_iter)

--n_rows: how many row of pictures to display, eg. 1 or not specified

--steps: number of denoising diffusion implicit models(DDIM) sampling steps in the image generation process. The more steps the better quality, but also more time and memory. default to 50

--seed: the seed to reproduce the same image, eg. 42 or 38, just a same number
```

### Create kaggle dataset to save result

```pip install kaggle```

create_dataset.py
```
from tools.generate_kaggle_dataset import create_kaggle_dataset
create_kaggle_dataset(
    dataset_dir=<..>,
    dataset_name="<kaggle_id>/<dataset_name>”,
    dataset_title=”<dataset_title>”,
    dataset_description=”<dataset_description>”,
    is_private=True
)
```