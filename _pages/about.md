---
permalink: /
title: "About Me"
author_profile: true
seo_description: "Academic page of Wahyu Andy who working as a PhD student in Industrial Engineering"
excerpt: "Academic page of Wahyu Andy who working as a PhD student in Industrial Engineering - excerpt"
redirect_from: 
  - /about/
  - /about.html
---

Hi! I am a PhD fellow student in the Industrial Engineering Department at [UiT The Arctic University of Norway](https://uit.no). Additionally, I am affiliated with [Telkom University - Surabaya Campus](https://surabaya.telkomuniversity.ac.id/) as a lecturer in the undergraduate program of the Industrial Engineering Department. Prior to my academic pursuits, I also gained several years of experience working in the IT industry.

Should you need further information about study program in Industrial Engineering Department at UiT, please visit our [website](https://uit.no/enhet/iit?p_dimension_id=210113). Meanwhile, if you are interested in continuing study in Indonesia, you can see more information [here](https://smb.telkomuniversity.ac.id/). 

Bio
======
* **Ph.D student in Industrial Engineering**, UiT The Arctic University of Norway, 2023 - present
* **M.Sc. in Industrial Engineering**, Pusan National University, Busan - South Korea, 2014 - 2016
  * An awardee of Korean Government Scholarship Program (KGSP), 2013
  * A former member of [BAE](https://baelab.pusan.ac.kr/baelab/63110/subview.do) lab
* **B.Sc. in Information System**, Institut Teknologi Sepuluh Nopember, Surabaya - Indonesia, 2005 - 2009

Like many other Jekyll-based GitHub Pages templates, Academic Pages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart's content without touching the content of your site. If you get to a point where you've broken something in Jekyll/HTML/CSS beyond repair, your markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over -- just be sure to save the markdown files! Finally, you can also write scripts that process the structured data on the site, such as [this one](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) that analyzes metadata in pages about talks to display [a map of every location you've given a talk](https://academicpages.github.io/talkmap.html).

Research
======
I am an active member of research groups 
1. [ArcLog](https://uit.no/research/arclog-en) research group focuses on creating secure and sustainable logistics operations and industrial production in the north.
2. [Intelligent Manufacturing and Logistics](https://uit.no/research/inmalog) research group focuses on development cutting-edge knowledge and technological solutions that promote human-centric production and logistics management
3. [Mascot - Mathematical Structures in Computations](https://uit.no/research/mascot) research group focuses on exploiting fundamental structures of mathematical computations, analyzing structural methods to reduce the complexity, as well as to adapt these methods to concrete applications in optimization, control theory, and robotics

Service
======
* Lecturer at Industrial Engineering Department, Institut Teknologi Telkom Surabaya, 2018 - Jul 2023
* Head of Marketing and Admission Office, Institut Teknologi Telkom Surabaya, Nov 2021 - Jul 2023
* Head of Research and Community Service Unit, Institut Teknologi Telkom Surabaya, Mar 2019 - Oct 2021
# * The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring Academic Pages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
