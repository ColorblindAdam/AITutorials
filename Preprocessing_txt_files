When Creating a Lora or model sometimes you need a lot .txt. 
This script will ask for the folder location and make a .txt file for each image.  
You can also add a prompt like "Dogs" and it'll put dogs in each .txt file.

```
import os
import glob

def create_txt_files(directory, content):
    # Change the current directory to the specified directory
    os.chdir(directory)

    # Get all .jpg and .png files
    image_files = glob.glob('*.jpg') + glob.glob('*.png')

    # For each image file
    for image_file in image_files:
        # Get the file name without the extension
        file_name = os.path.splitext(image_file)[0]

        # Create a .txt file with the same name
        with open(f'{file_name}.txt', 'w') as f:
            f.write(content)

    print('Text files have been created for each .jpg and .png file.')

def main():
    directory = input('Enter the path to your images folder: ')
    content = input('What Prompts do you want in the texts? ')
    create_txt_files(directory, content)

if __name__ == '__main__':
    main()
