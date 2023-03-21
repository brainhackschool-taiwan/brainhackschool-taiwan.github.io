---
layout: default
title: Writing scripts in python - Exercise
parent: Modules
nav_exclude: true
---

# Writing scripts in python - Exercise

## Description:

- This exercise is pretty much identical to that of [BrainHack School 2022](https://school.brainhackmtl.org/modules/python_scripts/), with some parts of the decsriptions revised/modified to hopefully make the instructions clearer. The crux of this assignment is to implement the `argparse` module in Python, which is an easy way to write user-friendly command-line interfaces and has a wide variety of applications. Please carefully read the background information in the next section.

## Background Info
- We'll be programming a key-based encryption and decryption system that is an adapted version of the Vigenère cipher: instead of using the 26 letters of the English alphabet, we'll be using all the unicode characters.
- The Vigenère cipher shifts the letters in the message to be encrypted by the index of the corresponding letter in the key. For instance, the encryption of the letter `B` with the key `D` will result in `new_index = index(B) + index(D) = 2 + 4 = 6`, represented by the 6th letter `F`. (⚠Note that what's meant by "index" here is the index of the letter in the alphabet, e.g., A = 1, B = 2, C = 3 so on and so forth, NOT the index of the letter in the string.)
- You will then pair up the letters in the message with those contained in the key one by one. The key is repeated if it is shorter than the message. For instance, if the message is `message` and the key is `key`, the pairs will be :
```
(m,k),
(e,e),
(s,y),
(s,k),
(a,e),
(g,y),
(e,k)
```
- For the letter indices, we won't be using the those corresponding to the 26-letter English alphabet, but their unicode indices, which can be easily obtained with the native Python function `ord`. The reverse operation, i.e., recovering the letter from a given unicode index is obtained with the native python function `chr`. There are 1114112 unicode characters handled by Python, so we'll have to make sure we have indices in the range 0 to 1114111. To ensure that, we can use values modulo 1114112, i.e., `encrypted_index = (ord(message_letter) + ord(key_letter)) % 1114112`. ("Modulo" is a widely used operation in message encryption, by the way.)

## Instructions:
### Step 1 - `useful_functions.py`
- Define the following three functions:
    + `encrypt_letter(letter, key)` : returns the encrypted letter with the key, e.g., `encrypt_letter('l', 'h')` should return `'Ô'`
    + `decrypt_letter(letter, key)` : returns the decrypted letter with the key, e.g., `decrypt_letter("Ô", "h")` should return `'l'`
    + `process_message(message, key, encrypt)`: returns the encrypted `message` using the letters in `key` if `encrypt == True`, and the decrypted `message` if `encrypt == False`
    + For instance,
      ```
      In[1]   process_message('coucou', 'clef', True)
      Out[1]  'ÆÛÚÉÒá'

      In[2]   process_message('ÆÛÚÉÒá', 'clef', False)
      Out[2]  'coucou'
      ```
      
### Step 2 - `cypher_script.py`
- Under the same firectory as `useful_functions.py`, create another file named `cypher_script.py` and `import useful_functions.py`
- Import the `argparse` module so the terminal user can call `cypher_script.py` with three arguments : `--message`, `--key`, and `--mode`
- `--message` is a text file (or the path to a text file), e.g., `msg_file.txt`, in which texts to be encryped/decrypted are listed in seperate lines:
```
Writing scripts
in
python
is so much
fun
```
- `--key` is a string that will be used as the key.
- `--mode` is a string that takes either `enc` or `dec` as its value to determine whether to encrypt or decrypt the messages.
- With the functions imported from `useful_functions.py` and `argparse` methods, create a function that encrypts or decrypts the texts in the message file using the key string as the key depending on the mode, and saves the results in a text file that has the same name as the message file but with a `_encrypted` or `_decrypted` suffix to the end. So for instance, calling `python cypher_script.py --message msg_file.txt --key my_key --mode enc` should create a `msg_file_encrypted.txt` file.
- The execution code of the function should be put under `if __name__ == "__main__"`, which, for certain practical purposes, allows you to execute the code when the file is run as a script, but not when it's imported as a module.
- You can test your script in the terminal with `msg_file.txt` first, then run the following command
```
wget https://raw.githubusercontent.com/BrainhackMTL/psy6983_2021/master/content/en/modules/python_scripts/message_encrypted.txt
```
and use `my_super_secret_key` as the key to **decrypt** the message.

## Assignment Submission:

- Upload a folder named `<Student_ID>_scripts` (e.g., `B05202021_scripts`) onto Google Drive. This folder should have the following four files:
    + `useful_functions.py`
    + `cypher_script.py`
    + the message to be encrypted obtained by running 
    ```
    wget https://raw.githubusercontent.com/BrainhackMTL/psy6983_2021/master/content/en/modules/python_scripts/message_encrypted.txt
    ```
    + the decrypted results of that message
- **Add brainhackschooltaiwan@gmail.com as an Editor of your entire `<Student_ID>_python_packaging` folder (we must be added, otherwise your email will fail to be uploaded to our Google Drive system)**, then get the link to your folder.
- Send an email with the subject title `[BHSTW] <Your_Student_ID> Writing scripts in python` (e.g., `[BHSTW] B05202021 Writing cripts in python`) to brainhackschooltaiwan@gmail.com, where the student ID should have all English letters capitalized, and the module name should be precisely the same as the example, with only the first letter of the first word capitalized. The link to your folder should be pasted in the email body
- You will receive an email reply titled `Receipt of submission` about 30 minutes after your submission email has been sent. This email will notify you whether your files have been successfully uploaded
- Please contact `Amanda Lin #5919` on Discord if your submission email keeps failing.

## Grading:

- You either pass (a 1 mark) or fail (a 0 mark) this assignment based on whether your decrypted message is correct.
- But don't worry if it isn't. One of the TAs will contact you on Discord and walk you through the exercise. A pass mark of 1 will also be given as long as you complete the exercise in the end.

