# Progress Reports

## Preliminary Progress Report: Repository Constructed
February 5, 2020

Added:
- `README` file that will contain a brief overview of the project
- `.gitignore` with some basics that should not be screened for upload by GitHub
- `LICENSE` file that will eventually contain a license delineating terms of use
- `project_plan` that contains a general overview of the project, and will be fleshed out in the future
- and of course this `progress_report` file

## 1st Progress Report: Rethinking the Project and Data Organization (Part I)
February 25, 2020

The first thing that became necessary was changing up my whole plan for this project, since
finding a corpus that fit my original idea of looking at a syntactic structure unique to
spoken Arabic wasn't panning out. In the search for a corpus to use, I came across the
[Arabic Learner Corpus](https://www.arabiclearnercorpus.com/) and have decided to use it
for this project. Please see my [Project Plan](https://github.com/Data-Science-for-Linguists-2020/Arabic-Learner-Corpus-Considerations/blob/master/project_plan.md)
for more detailed information.

Aside from rethinking my project's scope, this progress report focused on the following:

### 1. Attempting ~(and mostly completing)~ the data acquisition process
Finding a corpus was about the only thing that went to plan at this stage. The data are available under a Creative Commons license,
so I'm free to use them for non-commercial purposes as long as I give proper attribution to the original authors. The entire corpus
is freely available for download from the ALC website in a number of formats (plain text, XML, etc.), so this step was straightforward.

### 2. Making headway into cleaning and reorganizing the data
[Data organization](https://github.com/Data-Science-for-Linguists-2020/Arabic-Learner-Corpus-Considerations/blob/master/data_analysis/ALC_Data_Organization.ipynb)
was a process easier said than done, especially when working with XML and in a language other than English! BeautifulSoup gave me a lot of issues at first 
and wasn't reading the text in correctly. The hunch was that encoding was to blame, and a visit to Jevon's office hours (thanks Jevon!) helped get to the
bottom of everything. At this point, I'm able to read in the entries; next step is to get things into `dataframe` objects in `pandas` and make something
useful out of everything.

### 3. Thinking about a "data endgame" (final form, target total size, format, etc.)
You can look at my [test data](https://github.com/Data-Science-for-Linguists-2020/Arabic-Learner-Corpus-Considerations/tree/master/test_data) here. Right
now, I'm planning on leaving all of the original corpus files in their original forms and keeping them in a private folder for use. The plan is to
have `pandas` `dataframe` objects that contain the relevant tagged data from the original essays (learner L1, text, age, location, etc.) along with
additional information like text length and TTR^2 that I will compute myself. 

### 4. Devising a couple of options regarding the "sharing plan" of the data
The corpus I'm using comes with a Creative Commons license already, so I plan on using the same one and similarly allowing
anything that results from my work to be used for copying, redistribution, and adaptation for non-commercial purposes and
given proper attribution. I'm committed to this license because 1) it's in keeping with the licensure of the original work,
2) it aligns with principles of open science and data sharing, and 3) it doesn't seem to pose any ethical issues with identifiability
of the learners who were participants and had their data collected. That being said, I will refrain from sharing the entire corpus
on GitHub, since any reader will be able to download it from the original source. For more specific information, 
visit [my project's License page.](https://github.com/Data-Science-for-Linguists-2020/Arabic-Learner-Corpus-Considerations/blob/master/LICENSE.md)


## 2nd Progress Report: Data Organization (Part II)