The Qwen Image model was released a few days ago, and it's getting a lot of success.

It's great, probably the best, in prompt adherence, but if you want to generate some photo-realistic images, Qwen is not the best model around.

Qwen images are incredible, full of details, and extremely close to what you wrote in the prompt, but if I want to get a photo, the quality is really bad.Skin is flat; the look is cartoonish.So what could we do to fix this?LoRAs are coming... but it's the model that was not trained (probably) on real people's images, and a few LoRAs will not help too much.

The alternative is to apply some sort of "hi-res fix," a second pass with a different model.And here we have two strong choices, depending on what we want to achieve.

1) Flux Krea, the new model by BFL, which is, in my opinion, the best photorealistic model available today;

2) The good old SD1.5, SDXL, or Illustrious if you want to choose among thousands of LoRA and you want to generate NSFW images (some Illustrious realistic checkpoints are really good).

So, what should I use? What kind of workflow should I develop?Use Flux or SDXL as a second pass?

Why not give the user the choice?Add a loader for both models and let the user choose what kind of 2nd pass to apply.
