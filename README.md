
# Anime Model:
Our Model is designed to create Naruto Animation characters from text-to-images and image-to-image using Low-Rank Adaption(LoRA) Stable Diffusion.
You can download model from civitai [here](https://github.com/highplainscomputing/FineTune_StableDiffusion_Anime/blob/main/README.md#you-can-find-deployed-model-here)
 

## Pre-trained Model

In our project, we employ a **pre-trained model** known as "Stable Diffusion." This model has undergone training on a massive dataset consisting of 5 billion text-to-image pairs, making it a powerful foundation for various image generation tasks.

- Version: Stable Diffusion 1.5
- Additional Features: We use "Low Rank Adaption (LoRA)" for enhanced performance. LoRA allows the model to be trained effectively with minimal training data and a small .safetensors file, unlike models that require gigabytes of data.

## Fine Tune Dataset

Our dataset is derived from the popular Japanese anime, "Naruto Shippuden," and comprises approximately 1600 images, including fan art. You have the flexibility to use your dataset, but it must adhere to the proper format as outlined in the notebook.

- Note: If your dataset contains fewer than 20 images, consider enabling the "flip augmentation" feature.

For more details, please refer to the [Stable Diffusion Guide](https://civitai.com/models/22530).

## Trainer Extras

Our project offers various **trainer extras**, including hyperparameters that influence the training process:

- Number of repeats: Determine how many times you want to repeat your images.
- Number of epochs: Control the number of training epochs.
- Train Batch Size: Adjust the batch size for training.

### Learning Rates

- **UNet Learning Rate**: This parameter governs how fast your LoRA model absorbs information. Setting it too small may result in slow learning, while setting it too large may lead to overfitting. We recommend using a learning rate in the range of 1e-4 to 2e-4, with 5e-4 as a default value, for most situations.

- **Text Encoder Learning Rate**: While less critical, the text encoder learning rate aids in learning tags better. A good range for this parameter is between 1e-4 and 5e-5, typically being half or a fifth of the UNet learning rate.

- **Scheduler**: The scheduler guides the learning rate over time. We suggest using the cosine scheduler with 3 restarts for optimal performance. You can experiment with other scheduler options, such as constant or constant with warmup, to fine-tune your training process. A warmup ratio of 5% is a recommended default.

## Inference

To obtain inference from our project, follow these steps:

1. Run the first cell; it will take some time. When you see "Model loaded in 32.4s...", interrupt it.
2. Connect your Google Drive.
3. Provide the path to your LoRA model.
4. Run the last cell and open the Gradio link to interact with the model.

Check out a demo of the model trained on Naruto Anime Data [![Demo](https://img.shields.io/badge/Demo-View%20Demo-blue)](https://civitai.com/models/146475/naruto-or-lora).

Feel free to explore and experiment with our project. If you have any questions or feedback, please don't hesitate to reach out.


### You can find deployed model here

- [Naruto | LoRA](https://civitai.com/models/146475/naruto-or-lora)


