This Tutorial will teach you how to create a QR code with an existing image using Image2Image and QR Monster model controlnet.


QR Code - Image 2 Image with Automatic 1111

**Step 1**: Create an Image using your preferred image or use an existing image.
**Step 2**: Load Automatic1111 on Run Diffusion
**Step 3**: Select Img2Image Tab
**Step 4**: Change the Following Settings
**Model**: Any SD 1.5 Model capable of using Controlnet
**Image**: The image you wish to use
**Prompt**: I use the same prompt I used to create the image. But I tested it with images whose prompt I was not given and just guessed.
**Sampling Method**: DPM++ 2M Karras
**Denoising**: 0.4-.7 (Will explain below)
**Controlnet Settings**: Enabled, Pixel Perfect, Preview
**Preprocessor**: None
**Model**: control_v1p_sd15_qrcode_Monster
**Control Weight**: 2
**Control Mode**: Select Controlnet is More Important

**Step 5**: Adjust Denoising and Generate
Denoising must be adjusted for each image. I find the sweet spot to be .5 Hit generate. It
probably won’t scan the first pass.

**Step 6**: Send that new image to Img2Img and hit generate again. This time the QR code should
scan.

**Notes**:I feel a low denoising like .4 to .5 retains more of the original but may require you to run it
through a few times. .7 Seems to work after 1 or 2 passes but it changes the image. That is why
I recommend a lower denoise to retain as much of the original image as possible.

Original Image
![Olive Oil](https://github.com/ColorblindAdam/AITutorials/assets/130062936/43fcb975-8454-476e-920c-29e5e52ebfd1)

One Pass at .5 Denoising. It does not work yet.
![Step 2](https://github.com/ColorblindAdam/AITutorials/assets/130062936/b9b12a6f-d954-471f-b4af-93a8c4565517)

2nd Pass at .5 Denoising. It works now.
![00071-A glass olive oil bottle sitting on a marble counter, a granite background, dark contrast, deep shadows](https://github.com/ColorblindAdam/AITutorials/assets/130062936/f4752f95-fd7a-41e9-975c-6c38d68c6d0b)
