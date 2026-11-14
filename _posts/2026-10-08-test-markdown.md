---
layout: post
title: In Easier Terms
subtitle: What is the GitHub API?
---

Throughout this course, we learned about working with data and using R to interact with different tools and APIs. Since we worked closely with GitHUb why not explore the GitHub API and learn how it can help us access and analyze data from repositories!


## So what is the GitHub API?


**The GitHub API allows users to access information from GitHub programmatically. Instead of manually visiting a GitHub repository and looking through its information, we can use R to request that information directly.**


![GitHub API](/beautiful-jekyll/assets/img/how-to-interact-github-api.png)

**It can retrieve information such as:**

- Repository information
- Users
- Issues
- Pull Requests
- Commits
- Stars and forks
- Repository activity


Here's the example code you can use:

~~~
</>R
library(gh)

repo_info <- gh("/repos/r-lib/gh")

repo_info$name
repo_info$description
repo_info$stargazers_count
repo_info$forks_count
~~~

Now here is the same code when you place a GitHub repository to try:

~~~
</>R
repo_info <- gh("/repos/mgarc427/montyhall")

repo_info$name
repo_info$description
repo_info$stargazers_count
repo_info$forks_count
~~~

![GitHub API](/beautiful-jekyll/assets/img/GitHub Example.png)

**Try it out with your montyhall project!**
