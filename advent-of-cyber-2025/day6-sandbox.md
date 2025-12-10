## Overview
When we test malware, we can look at it in two ways: static or dynamic.

## Description
1. **Static**  
We do not run the file at all.  
Pestudio lets the analyst peek inside the file and see useful details without waking it up.

2. **Dynamic**  
We actually run the file but inside a safe environment.  
Regshot takes a snapshot of the registry.  
We take a baseline before the malware runs, then another snapshot after.  
Now we can spot the changes and see what sneaky stuff the malware tried to add.

## Registry Key

Think of the registry like a giant recipe book.  
Startup programs are the dishes the computer cooks.  
Windows is the chef who reads the book and decides what to serve.

Inside the registry, Windows stores a huge amount of settings, such as  
what runs at startup, user preferences, system settings, application info, and many more.

## Why this Matters?
Testing a software is an integral part of cybersecurity. It is important to do it in a safe env so i won't affect other devices should things go south. 