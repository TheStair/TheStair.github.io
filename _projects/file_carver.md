---
layout: default
title:  "FileRecovery"
date:   2024-11-01
categories: School Projects
---

[Github Repo](https://github.com/TheStair/FileRecovery)

# FileRecovery Python Script
This python script uses file signatures to extract files from binary blobs. Currently, this project can carve files of the following types pdf, gif, jpg, png, and avi.

First, I defined a dictionary of the required filetypes containing their start of file signatures and end of file signatures. Then the script iterates through this dictionary searching the input file for the starting byte literal strings. If a starting sequence is found, the file is carved, either using the EOF marker or known filesize.

After the file is carved, the script searches the rest of the file for remaining file headers of the specific type. After the entire disk image/binary blob has been searched, the script repeats with the next filetype.

After these files are carved, they are hashed to verify file integrity and saved in an output directory.

Usage: "Python3 FileRecovery.py \<input-file\>