# Dataset_Maker_Anime

- First run the Dataset Maker Anime file
- Connect it to your Google Drive for Dataset purpose 
- Afterwards upload your file into your Loras/[project_name]/dataset folder.
- All process is automated then you can provide your global activation tags and other functionalities are also provided.
 
# Lora Trainer Anime

In this file you need to look 5 things 
- [project_name] provide a complete name for your project that you provided in Dataset_Maker_Anime file.
- num_repeats
- epochs
- train batch size

use below strategies, it works well.

- 10 images × 10 repeats × 20 epochs ÷ 2 batch size = 1000 steps
- 20 images × 10 repeats × 10 epochs ÷ 2 batch size = 1000 steps
- 100 images × 3 repeats × 10 epochs ÷ 2 batch size = 1500 steps
- 400 images × 1 repeat × 10 epochs ÷ 2 batch size = 2000 steps
- 1000 images × 1 repeat × 10 epochs ÷ 3 batch size = 3300 steps

check flip aug if your dataset has less than 20 images.

for more details check out [Stable Diffusion Guide](https://civitai.com/models/22530)

# Inference 
- run the first cell, it will take a while. When you see "Model loaded in 32.4s..." interrupt it.
- Connect your drive
- give your LoRA models path.
- Run the last cell and open Gradio link
 
 Check out my model that I trained on Naruto Anime Data [![Demo](https://img.shields.io/badge/Demo-View%20Demo-blue)](https://civitai.com/models/146475/naruto-or-lora)

 
