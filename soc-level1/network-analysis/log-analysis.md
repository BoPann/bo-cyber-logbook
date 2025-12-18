---
creation date: 2025-12-17 12:34
modified: 2025-12-17 12:39
tags:
  - cyber/linux
  - cyber/tool
---
# Log Analysis

## Overview
Log is a record of events. Part of what analysts do is to know how to extract valuable information from a pile of logs.  

## Description
While analyzing log, we want to have an idea of what the fields look like. This is easy if we are using GUI tool like Splunk. We simply nevagate to the left panel to see them (we can also add them to the filter, too) 

However, in **command line Interface** environment, this can get really overwhelming. In my experience, it typically involves these steps: 
- head file - we want to have an idea of how it looks like. What fields does it have? 
- cut file - this steps is extracting the field we want and also make it less noise. 
	- `cut [delimiter] file -f3-5 | sort | uniq -c` 


>last modified: 2025-12-17 12:39