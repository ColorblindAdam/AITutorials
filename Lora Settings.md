These are my old Lora Settings. Which I used to create a science Cell model and a Tardigrade model on Run Diffusions.  I am not sure if they are still the best settings but haven't had time to check.  Here they are if you want to try them. 

**Preprocess Images**
On a Small or Medium Box.

Create a Folder /mnt/private/name_your_project

Put your images in that folder your named can be jpeg or png.

Create a second folder /mnt/private/name_your_project/train

*Be aware train/dreambooth are case sensitive when it comes to your folder names

Train → Preprocess Images → Source Directory box: /mnt/private/name_your_project

Train → Preprocess Images → Destination directory box: /mnt/private/name_your_project/train

Select Create flipped copies if you are doing a person or object.  Also click USE BLIP for Caption if you are doing non anime.  For Anime use Deepbooru.

Click Preprocess. This will put all the images in that /mnt/private/name_your_project/train folder you created with the appropriate .txt files.

You can edit the text files as needed.

**Lora Settings**

This assumes that you already have a dataset with your images and .txt files ready.

**1.**  Start a Medium or Large Box

**2.** Click on the Dreambooth Tab

Click The button that says Create.  Select the source checkpoint this is the model you are basing your Lora on.  Select create model.

**3.** Settings Tab

Check Use Lora.

Training steps Per Image: 100-128

Amount of Time to Pause between epochs: .3 seconds to 60 seconds.

Learning rate if you use lion 0.00005, 8bitAdam 0.0001.  8Bit Adam is Standard

Xformer: will speed up the Process but can cause more mutations like deformed fingers/hands. 

Mixed precision: fp16

At the bottom under Advanced Options: Sanity Samples. Go ahead and fill that out as if you were prompting for the image so that you can see examples.

**4**. Concept Tab

Enter your dataset director: /mnt/private/name_of_folder_/train

 Your dataset can be stored in the train folder. 

Instance Token: Is the unique token you are creating that would activate your Lora. Like “John48”

Training Prompt: A photo of John48

Class prompt: A Photo of a Person

Negative Prompt: blurry, bad quality, blahblah

Number of samples: 2

Seed: Don’t use random use the same seed so you can see the changes over time. (assuming UI doesn’t freeze up like it enjoys doing)

**5.** Saving Tab

Save EMA Weights should be checked.

Custom Model Name: Enter a name example: “John48”

Uncheck All the checkpoints otherwise it’ll end up like 4gbs and you don’t need that with a Lora.

Lora Text Encoder Rank: 128

Check: Generate Lora weights during training 

Check: Generate Long Lora weights for extra networks

Check: Generate weights when canceled.

At the Top click Save Settings

**Click Train**



