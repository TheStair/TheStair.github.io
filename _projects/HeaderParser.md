---
layout: default
title:  "Parser for ELF and PE Headers in Python"
date:   2025-02-24
categories: [Python, Software Reverse Engineering, School Projects]
tags: [Python, HeaderParser, Executables, ELF, PE]
---
# Header Parser

This Semester, I am taking a course in Binary Program Analysis. For the first project, I am writing a tool to parse ELF and PE Headers.

# ELF Parser

Due to the simplicity and clear documentation online regarding ELF Headers, this is where I decided to begin. Currently my script parses the ELF File header, Program Header Table, and the Section Header Table. I managed to match the output of the built in tool, readelf, for both 32 and 64 bit ELF binaries.

# PE Parser

Now that I have program functionality on ELF Headers, my next goal is to parse PE headers.

