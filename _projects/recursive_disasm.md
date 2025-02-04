---
layout: default
title:  "Recursive Disassembler"
date:   2025-01-31
categories: School Projects
---
# Recursive Disassembler (Work-In-Progress)  

This Semester, I am taking a course in Binary Program Analysis. For the first project, I plan to write a Recursive Descent Disassembler for ELF files in python using the Capstone Library. I will update this post with my progress, and cool things I learn along the way.

# Initial Ideas (02/04/2025)

With this just being one class, I am a little bit nervous about biting off more than I can chew, and attempting to do too much with the time I have. However, I think I have a good idea for my project. I want to leave room for future additions and make my life in future additions a lot easier. I am going to start with ELF Files.

I want to use three pandas dataframes. One dataframe dedicated to functions, with the function address as the key, and it's instruction addresses as the data and possibly a value for the symbol liked to it (if present in the binary).  

The next dataframe, will hold instruction Addresses, Opcode, Source, and Target. This may help to later define basic blocks to create control flow graphs. This is my **first goal**. To create an index of instructions by recursive descent dissassembly.

The final dataframe, will be for basic blocks. With an assigned id, contained instructions, and other control flow data. (This is for future work)

# Process