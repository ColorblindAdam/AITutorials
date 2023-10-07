The digital art world is always alive with new trends, and lately, QR code art has taken center stage. If you've been intrigued by the creative pieces gracing platforms like Twitter and other online avenues, then you're witnessing the magic of Stable Diffusion. While techniques such as Controlnet, Canny, and Zoe Depth maps have provided artists with avenues to experiment in the past, QR Code Monster simplifies the process, requiring minimal adjustments for the perfect result. It's not just a trend—it's a welcoming art evolution, and as a newbie, you're about to embark on a delightful journey of creativity. 

Begin by initializing Automatic 1111. Given the fast-paced nature of our lives today, many, including myself, often lean towards medium servers for efficiency. However, if you find yourself with a leisurely pace and time on your hands, a small server serves just as well. The choice ultimately hinges on your time availability and budget. For this specific project, rest assured, there's no need for a larger setup.
**Step 1: Select your Checkpoint** 
To embark on this journey, select your desired model for SD 1.5. For those following along with my preferences, I'm opting for Dreamshaper 8. But don’t let that limit you; various models may be used I have tested this on 5 models and all worked. There's room for experimentation and personal preference.

  ![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/8f739916-e5ad-439e-bfd5-23b6e12a9783)

**Step 2: Generate our initial Images and Save them**
Now let’s generate a quick image to work with. I’m just going to use the first image that pops up just to show you how easy this can be.
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/73f89579-3cdd-418f-a5dd-172fc551b386)

**Prompt**: cartoon,black and white image, illustration, checkered background, black squares, white squares
**Negative**:color, blurry, ugly
**Seed**:3707886602

If you would like to follow along feel free to right click and save this image to use or generate one yourself.
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/caa8548f-4c71-42c1-a3be-1a3d09f5170b)

Let's do another example, this time using a character. This will show how flexible this method is. We'll use simple steps so it's easy for beginners. I'll pick the first picture that shows up. Let's keep it simple and fun.
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/147c1fe8-9d6f-4df3-82df-957cc3959aec)
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/c24ac918-9c5f-4f40-b4fb-8d9f1ed6c0d9)

Now let’s create interesting art!

**Step 3: Adjust your Settings**
**Checkpoint/Model**: up to you (I’m using Dreamshaper 8)
**Sampling Method**: DPM++ 2M Karras
**Steps**: 40+  I like it around 50-60 personally.
**CFG**: 7-9.5

![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/b7900869-5c61-4f99-b368-eceb0ad83acd)

**Controlnet settings**:

1. Enable
2. Pixel Perfect
3. Preprocessor: none
4. **Model**: control_v1p_sd15_qrcode_monster [a6e58995]
5. Image: The checkered Image we just created

![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/85b22bf7-999a-4b59-9a07-099d7f1655ce)

**Step 4: Time to be a prompt Engineer**
You're well-prepared now is where you get to let your creativity shine. I'll provide a foundational example to get you started. It's essential to note that the potential here is immense; it's a blend of your selected seed and the ingenuity of your prompts.

**Prompt**: Beautiful flower garden, background blue sky,  photograph, best quality, 8k, high resolution, award winning photograph, oil painting
**Neg**:  blurry, ugly, watermark, logo, text, website, bad quality,
**Seed**:2049251640

![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/4063e225-60d2-4b44-8570-8127dbeb7bad)

**Next Prompt**: A Japanese woman wearing a kimono, photograph, best quality, 8k, high resolution, award winning photograph, oil painting
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/832effd3-4dfd-4fa9-ba4b-dadb4104045a)

**Prompt**: Cybernetic Mouse, photograph, best quality, 8k, high resolution, award winning photograph, oil painting
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/ad35347e-0c53-4701-845b-f97676861a22)

Those are just a few small examples to get you started.  Now let’s move on to the character example..  

**Step 5: Character example**

Go down to Controlnet and swap out the images for the cute cats.

![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/f773b615-df21-42e1-97f9-4906bc087222)

**Prompt**: A beautiful mountain with an alpine forest and glacial lake, photograph, best quality, 8k, high resolution, award winning photograph, oil painting
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/3b35f8d0-4196-4523-86a3-dccde4ec4fa1)

If you zoom in it looks like a beautiful mountain scene.  But if you make the image smaller on your screen or step away from the screen. You can see your cats in the image.

**New Prompt**: An assortment of glass bottles, photograph, best quality, 8k, high resolution, award winning photograph, oil painting
![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/76551ccc-3e74-4ebb-9513-baec6b3ffcca)

You can use numerous styles and prompts to change it up.  I’ve kept the same seed just for simplicity for the tutorial.

**Another prompt**: A tropical forest, photograph, best quality, 8k, high resolution, award winning photograph

![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/897fe2f6-1b86-4952-95cb-94b4b103fded)

Hope you enjoyed and please make sure to share on the Run Diffusion Discord in #showcase the works you create feel free to tag me as I love this style of art. 

![image](https://github.com/ColorblindAdam/Stablediffusionscripts/assets/130062936/dec3fab1-61a6-4cc2-abd7-07c35e82394a)

