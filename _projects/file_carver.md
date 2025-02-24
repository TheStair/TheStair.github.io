---
layout: default
title:  "Recovering Hidden Files from Binary Data with Python"
date:   2024-11-01
categories: [Python, File Recovery, Digital Forensics, School Projects]
tags: [Python, FileRecovery, FileCarving]
---

# Recovering Hidden Files from Binary Data with Python

In this post, I’ll walk you through a Python script designed to extract embedded files from binary blobs by leveraging file signatures. Whether you’re dealing with disk images or raw binary dumps, this tool is handy for carving out specific file types. Currently, it supports PDF, GIF, JPG, PNG, and AVI formats.

## How It Works

### 1. Defining File Signatures

The process starts by defining a dictionary of file types paired with their unique start-of-file (SOF) and end-of-file (EOF) markers. These markers are essential to accurately pinpoint where each file begins and ends within the binary data.

### 2. Iterating Through the Binary Blob

The script then iterates through the input file, searching for these starting byte sequences. Once it detects a file header, the script “carves” the file—using the EOF marker or a known file size—to extract it from the blob.

### 3. Scanning for Additional Headers

After carving out the first instance, the script continues scanning the rest of the binary for any remaining headers of the same type. This process repeats for every file type defined in the dictionary until the entire binary blob has been thoroughly examined.

### 4. Verifying and Saving the Files

Once all potential files have been extracted, each one is hashed to verify its integrity. Finally, the recovered files are saved to a designated output directory, ready for use.

## How to Use the Script

Simply run the following command in your terminal to start the recovery process:

```bash
python3 FileRecovery.py <input-file>
```
[Github Repo](https://github.com/TheStair/FileRecovery)