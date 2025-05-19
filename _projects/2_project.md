---
layout: page
title: Utility Bill Calculator
description: Python script with a simple GUI for non-technical users
img: assets/img/utility_bg.jpg
importance: 1
category: work
giscus_comments: false
---
[Github repo: technical documentation and modules](https://github.com/Nmension/Utility_Bill_Calculator).
<br />

### **Context:**

This project is custom-made for a specific residence that has 5 houses to rent: B1, B2, B3, B4, B5 plus a reception for the security personnel. Each of these buildings consumes different amounts of electricity (in kWh) and water (in m3) every month. They are all equipped with divisional meters that record their respective consumption indices and are used to calculate their individual amounts to be paid. 
  This situation arises because the electricity/water bill is directly grouped for the whole residence, thus the need to divide the required ammount requested by the provider among the tenants according to their individual consumptions. 

In the past, I created a spreadsheet that automated the calculations by implementing formulas between cells, but since end users were not familiar with spreadsheets, it was still not very convenient for them, although it was better than doing everything by hand, which is also an error-prone process. <br />
That's where the idea to create some kind of front end interface that would simplify the process for non-technical users came from. 

<br />

### **Setup summary:**
1. A file in .exe format for easier distribution purposes created using Pyinstaller. 
1. A file in .py format that contains the backend part and generates the frontend GUI.
<br />

One difficulty I encountered was when creating the windows executable file. I tried Nuitka but every attempt ended up with the .exe not launching though the compilation completed without errors. I knew the problem wasn't from the script as it worked well when launched using the Python Interpreter. That's why I switched to Pyinstaller as a short term solution.<br /> 
Then, one problem you might encounter with Pyinstaller as I did, was that my antivirus solution (Avira) prevented the .exe file from being created and false-positively flagged it as malware since it had no certificate. 
The work-around I found was to disable my antivirus until the bundling was done as it would trigger only when creating the .exe and not after. 

  If you are interested in making changes in the code or follow the process I went through then, here's the command I used to generate the .exe file:
```bash
pip install pyinstaller
pyinstaller --onefile --collect-data sv_ttk --noconsole --icon=house.ico Calculateur_de_decompte_energetique.py --version-file file_version_info.txt
```
  To make that command work, we first need [pip, (package installer python)](https://pip.pypa.io/en/stable/installation/#get-pip-py), installed but also, to [generate](https://pypi.org/project/pyinstaller_versionfile) a _file_version_info.txt_ for the metadata that will be linked to the file. 
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/utility_screenshot.png" title="Utility Bill Calculator Preview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Here's a preview of how the GUI looks like when the .exe file is directly executed or the .py file through a Python Interpreter.
</div>
I decided to use a basic tab design to make it more intuitive and easier to navigate through than with a spreadsheet when the end user is inputing data or correcting anything. 
<br />
<br />

#### - To-do list: 
  - feature: improve modularity with the ability to edit the number of buildings in the residence;
  - feature: add a dropdown menu for language selection with english support;
  - feature: individual .docx or .pdf receipt generation;
  - refactor: improve code design to make the end app faster;
  - chore: improve the GUI using more contrasting colors. 
  