---
title: Blogging Guide 
date: 2023-09-29 12:37:30 +0300
categories: [Blog,Github Pages]
tags: [blogging]
---
# How to Set up a blog on Github pages

There are many benefits - personal and professional - of having a personal blog. It gives you a platform to express your creative ideas and share knowledge to a large audience. Also, through showcasing your expertise and skills, you attract the attention of potential employers, clients and even collaborators hence putting you in a pole position for new opportunities.

Here, I'll walk you through step-by-step on how to setup a blog on github pages.

### Content Breakdown
>Requirements

>Installation

>Resources

### Requirements
1. Github account - Sign up for a free account at [](https://github.com/signup)
2. Visual Studio code - Download and install VScode from [](https://code.visualstudio.com/download)
3. Git - Download and install Git from [](https://git-scm.com/download/win)

### Installation
To setup a clean, customizable and responsive blog site, we will integrate Jekyll - a static site generator - with Github pages. 
First, let's install Ruby which enables Jekyll to run smoothly. Download Ruby+Devkit 3.2.2-1(x64) (latest version at time of this writing) from [](https://rubyinstaller.org/downloads/)

![img-description](/assets/img/jekyll/1.png)
_figure 1_

Install using the default setting and ensure the option to "Run 'ridk install" is checked. Click on Finish

![img-description](/assets/img/jekyll/2.png)
_figure 2_

Upon clicking finish, you will be prompted to choose what components to install. Click Enter.

![img-description](/assets/img/jekyll/3.png)
_figure 3_

After it completes, initiate command prompt and run the following command to install all the dependencies
```powershell
gem install jekyll bundler
```

![img-description](/assets/img/jekyll/4.png)
_figure 4_

Congratulations for reaching this far! Let's go on...

Next, proceed to https://github.com/cotes2020/chirpy-starter. Click on 'Use this template' to toggle the drop-down and select Create a new repository.

![img-description](/assets/img/jekyll/5.png)
_figure 5_

Careful here!

Under Repository name, enter the name of your github page. Syntax: *your_github_username.github.io*  
Select Public and finally Create repository. 

![img-description](/assets/img/jekyll/6.png)
_figure 6_

Once done creating the repo, Click on 'Code' to toggle the drop-down and copy the url as hightlighted below
![img-description](/assets/img/jekyll/7.png)
_figure 7_

Open Visual Studio and select 'Clone Git Repository' as shown below.  
![img-description](/assets/img/jekyll/8a.png)
_figure 8a_

 Paste the copied url and hit Enter.  
 Select your desired destination folder and 'Select as Repository Destination'.

![img-description](/assets/img/jekyll/8b.png)
_figure 8b_

When prompted, open the cloned repository. It should resemble the one below.

![img-description](/assets/img/jekyll/8c.png)
_figure 8c_

So far so good. Let's keep going on...

Within Visual Studio, open a terminal as guided below and run the following command. 
````powershell
bundle
````
This will bundle up all the jekyll dependencies.

![img-description](/assets/img/jekyll/11.png)
_figure 9_

As per theme's documentation, we need to copy some critical files from the theme's gem to jekyll's site. See below
![img-description](/assets/img/jekyll/d.png)
_figure 10_

Let us run the following command to locate these files.
````powershell
bundle info --path jekyll-theme-chirpy
````
![img-description](/assets/img/jekyll/12.png)
_figure 11_

Follow the path i.e. C:/Ruby32-x64/lib/ruby/gems/3.2.0/gems/jekyll-theme-chirpy-6.2.2  
Below, A is the jekyll site and B is the theme's gem. So we copy *_config.yml*, *_plugins*, *_tabs*, *index.html* from B to A

![img-description](/assets/img/jekyll/13.png)
_figure 12_

Almost there!

Let's go ahead and stage our changes, commit them and push them to the remote repo  
Use the following commands 
```powershell
git add .
git commit -m <message>
git push
```
**Note: The angle brackets are not part of message**

![img-description](/assets/img/jekyll/14.png)
_figure 13_

It is likely you'll get a request to authorize Git-ecosystem. Accept the request
![img-description](/assets/img/jekyll/15.png)
_figure 14_

We can see the changes in our repository by clicking on the Actions tab.  
Once the process is successfully complete, click on the link beneath deploy

![img-description](/assets/img/jekyll/16.png)
_figure 15_

Congratulation! Your site is up and running.  
Just some customizations now.

![img-description](/assets/img/jekyll/17.png)
_figure 16_

To change the default configurations, we will edit the _config.yml file. Here you can modify the title, tag line, avatar, among other settings.  
Make sure to input the your github.io link in the url field

![img-description](/assets/img/jekyll/18.png)
_figure 17_

In the next post, I will cover the following:
>Creating our first post

>Troubleshooting
### Resources
For further readings, please refer to the below resources
1. https://jekyllrb.com/docs/installation/
2. https://github.com/cotes2020/chirpy-starter
3. https://github.com/cotes2020/jekyll-theme-chirpy#readme