# Generate Password List From Wordlist in Python

This Python script can generate potential passwords from a list of words by appending characters to the end of each word. You have the option to specify your own set of characters and export the results to a .txt file.

## Clone

```
# Clone this repository
$ git clone https://github.com/yZ1337/python-passlist-gen.git
```

## Install Libraries

```
# Will be installed automatically on run, but you can install manually:
$ pip install colorama
$ pip install requests
$ pip install bs4
```

## Usage

### Pass list generator
```
$ python3 passlistgen.py -h

usage: passlistgen.py [-h] [-w WORDLIST] [-a ADD] [-o OUTPUT]

Modify words in a file by appending characters and save output.

options:
  -h, --help            show this help message and exit
  -w WORDLIST, --wordlist WORDLIST
                        Path to the wordlist file
  -a ADD, --add ADD     Characters to use, comma separated
  -o OUTPUT, --output OUTPUT
                        File to save the modified words
  -fe FIDNEMAILS, --findemails FIDNEMAILS
                        Find emails on a website by URL
                        and outputs it to a file.
```

```
# Generates output file: new-pass-list.txt
$ python3 passlistgen.py -w old-pass-list.txt -o new-pass-list.txt
```

```
# Generates output file: new-pass-list.txt with specified special characters
$ python3 passlistgen.py -w old-pass-list.txt -a "!, 01, @, &, 7777, 1234, 0123" -o new-pass-list.txt
```

### Email finder
```
$ python3 main.py -fe https://website.com
#############################
#      Created by: yZ       #
#############################

Scanning for emails...

[+] firstname.lastname@example.com.Learn

[INFO] 1 found on the website.
[SUCCESS] File saved to: found_emails_2024-03-14.txt

```

## To Do List

 - [x] Check the website page for emails
 - [ ] Search the website for potential words/passwords
 - [ ] Crawl the entire website, not just one page, to find emails
 - [ ] Insert characters within a word, not only at the end

I will try to provide more updates in the future!
