This code is for creating datasets for training LoRa.

This code gives you 3 options.

1. Deletes all information in .txt files in a specific folder.  (There is a warning when selecting this option)
2. Adds a prompt to all .txt files in a specific folder. (When adding a prompt you may also want to add a comma )
3. Removes a prompt from all .txt files in a specific folder. (Don't forget to delete extra commas)

```
import os
import glob

def clear_txt_files(directory):
    # Change the current directory to the specified directory
    os.chdir(directory)

    # Get all .txt files
    txt_files = glob.glob('*.txt')

    # For each .txt file
    for txt_file in txt_files:
        # Open the .txt file and overwrite it with empty content
        with open(txt_file, 'w') as f:
            f.write('')

    print('All text files have been cleared.')

def remove_prompt(directory, prompt):
    os.chdir(directory)

    txt_files = glob.glob('*.txt')

    for txt_file in txt_files:
        with open(txt_file, 'r') as f:
            lines = f.readlines()
        with open(txt_file, 'w') as f:
            for line in lines:
                f.write(line.replace(',' + prompt, '').replace(prompt, ''))

    print('Prompt removed from all text files.')

def update_txt_files(directory, additional_content):
    os.chdir(directory)

    txt_files = glob.glob('*.txt')

    for txt_file in txt_files:
        with open(txt_file, 'a') as f:
            f.write(additional_content)

    print('Text files have been updated.')

def main():
    print("1: Clear all .txt files")
    print("2: Remove a specific prompt")
    print("3: Add a prompt")
    option = input('Enter your option: ')

    directory = input('Enter the path to your folder: ')

    if option == '1':
        warning = "This option will delete all information found in the .txt files."
        print(warning)
        proceed = input('Do you want to continue? Y/N ')
        if proceed.lower() == 'y':
            clear_txt_files(directory)
    elif option == '2':
        prompt = input('Enter the prompt to remove: ')
        remove_prompt(directory, prompt)
    elif option == '3':
        prompt = input('Enter the prompt to add: ')
        update_txt_files(directory, prompt)
    else:
        print('Invalid option.')

if __name__ == '__main__':
    main()
