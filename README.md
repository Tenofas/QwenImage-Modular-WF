The Qwen Image model was released a few days ago, and it's getting a lot of success.

It's great, probably the best, in prompt adherence, but if you want to generate some photo-realistic images, Qwen is not the best model around.

Qwen images are incredible, full of details, and extremely close to what you wrote in the prompt, but if I want to get a photo, the quality is really bad.Skin is flat; the look is cartoonish.So what could we do to fix this?LoRAs are coming... but it's the model that was not trained (probably) on real people's images, and a few LoRAs will not help too much.

The alternative is to apply some sort of "hi-res fix," a second pass with a different model.And here we have two strong choices, depending on what we want to achieve.

1) Flux Krea, the new model by BFL, which is, in my opinion, the best photorealistic model available today;

2) The good old SD1.5, SDXL, or Illustrious if you want to choose among thousands of LoRA and you want to generate NSFW images (some Illustrious realistic checkpoints are really good).

So, what should I use? What kind of workflow should I develop?Use Flux or SDXL as a second pass?

Why not give the user the choice?Add a loader for both models and let the user choose what kind of 2nd pass to apply.

This workflow will generate a high-res Qwen image, and then the image will go through a 2nd pass with the model (with LoRAs if you want to use them) of your choice.

The image then can be sent to each one of the modules:1) Face detailer (to improve the details of faces in the image), 2) Ultimate SD Upscaler, and 3) Save the final image.

Warning: this workflow was developed for photorealistic images. If you just want to generate illustrations, cartoons, anime, or images like these, you don't need a second pass, as the Qwen model is already perfect by itself for these kinds of images.

This workflow was tested on Runpod with a rtx 5090 gpu, and using the standard models (Qwen bf16 and Flux Krea fp16) I had no trouble or OOM errors. If your GPU has less than 32GB it is probable that you need to use the fp8 models or the quantized GGUF models.

As another alternative, you can download the "Qwen Image WAN2.2 Modular WF v1.0.json" workflow file, if you want to use Wan2.2 model for second pass in place of Flux/SDXL/Illustrious.
