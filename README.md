# Dataset_Maker_Anime

- First run the Dataset Maker Anime file
- Connect it to your Google Drive for Dataset purpose 
- Afterwards upload your file into your Loras/[project_name]/dataset folder.
- All process is automated then you can provide your global activation tags and other functionalities are also provided.
 
# Pre trained Model

- We use stable Diffusion(pre-trained) Model which is trained on 5 billions text-to-image pairs
- Stable Diffusion version 1.5
- Use Low Rank Adaption(LoRA) which has it's own advantages.
- With LoRA you can trained it with low training data along with small .safetensors file, unlike GB's of file.

# Fine Tune Dataset
- Dataset is from Japenese Popular Anime Naruto Shippuden consists of almost 1600 images including fanart
- Use your own dataset but it should be in proper format according to notebook designed

check flip aug if your dataset has less than 20 images.

for more details check out [Stable Diffusion Guide](https://civitai.com/models/22530)

# Trainer Extras
There are many Hyperparameters like unet learning rate, text encoder learning rate, etc.
Look 3 of them only
- Number of repeats : How many times do you want to repeat your images.
- Number of epochs
- Train Batch Size
## Learning 
- The unet learning rate dictates how fast your Lora will absorb information. Like with steps, if it's too small the Lora won't do anything, and if it's too large the Lora will deepfry every image you generate. There's a flexible range of working values, specially since you can change the intensity of the lora in prompts. Assuming you set dim between 8 and 32 (see below), I recommend 5e-4 unet for almost all situations. If you want a slow simmer, 1e-4 or 2e-4 will be better. Note that these are in scientific notation: 1e-4 = 0.0001

- The text encoder learning rate is less important, specially for styles. It helps learn tags better, but it'll still learn them without it. It is generally accepted that it should be either half or a fifth of the unet, good values include 1e-4 or 5e-5. Use google as a calculator if you find these small values confusing.

- The scheduler guides the learning rate over time. This is not critical, but still helps. I always use cosine with 3 restarts, which I personally feel like it keeps the Lora "fresh". Feel free to experiment with cosine, constant, and constant with warmup. Can't go wrong with those. There's also the warmup ratio which should help the training start efficiently, and the default of 5% works well.

# Inference 
- run the first cell, it will take a while. When you see "Model loaded in 32.4s..." interrupt it.
- Connect your drive
- give your LoRA models path.
- Run the last cell and open Gradio link
 
 Check out my model that I trained on Naruto Anime Data [![Demo](https://img.shields.io/badge/Demo-View%20Demo-blue)](https://civitai.com/models/146475/naruto-or-lora)

 
