If you want to add to the .txt files in a folder all at once you can use this prompt.

Example: If you type Dog.  It'll add ",dog" to all the .txt files in a folder you select. 

```
import os
import glob

def update_txt_files(directory, additional_content):
    # Change the current directory to the specified directory
    os.chdir(directory)

    # Get all .txt files
    txt_files = glob.glob('*.txt')

    # For each .txt file
    for txt_file in txt_files:
        # Open the .txt file
        with open(txt_file, 'a') as f:
            # Write the additional content to the end of the file
            f.write(', ' + additional_content)

    print('Text files have been updated.')

def main():
    directory = input('Enter the path to your folder: ')
    additional_content = input('What content do you want to add to the end of the texts? ')
    update_txt_files(directory, additional_content)

if __name__ == '__main__':
    main()
```
