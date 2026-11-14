---
layout: post
title: "The R Package: gh"
subtitle: "An interface between R and the GitHub API"
cover-img: /assets/img/github_PJ_McDonnell_shutterstock.jpg
thumbnail-img: /assets/img/GitHub Neon.jpeg
share-img: /assets/img/github_PJ_McDonnell_shutterstock.jpg
tags: [books, test]
date: 2026-10-08
---

**The R package gh provides an interface between R and the GitHub API, making it possible to send requests to GitHub directly from R.**

```r
library(gh)
```

**The API returns information about the repository, including its name, description, number of stars, and number of forks. Because the response is returned as an R object, I can access individual pieces of data easily.**

## What type of data does it return?

The GitHub API uses **JSON (JavaScript Object Notation)** to send information. The gh package processes the API response and makes the information available as R objects, such as lists. This allows you to work with GitHub data directly in R.

**GitHub → GitHub API → JSON → gh package → R**

One benefit of using an API is that you don't have to manually collect information from GitHub. I can use R to request the information I need and then use it for analysis. This could be useful when working with multiple repositories or tracking changes over time.

## Let's do a step by step:

Install the gh package onto your r studio using the code above

Then you will load the library

You can then search APIs on Github
![GitHub API](/beautiful-jekyll/assets/img/Step 1.png)

Once you chose you will then insert the API into this r code 

library(gh)

repo_info <- gh("/repos/r-lib/gh")

**When you insert into the code make sure you grab the user and name of the package**

**repo_info <- gh("/repos/NoahZinsmeister/Rbnb")**

![GitHub API](/beautiful-jekyll/assets/img/Step 3.png)

Process the returned data as R objects

![GitHub API](/beautiful-jekyll/assets/img/Step 4.png)

**This list can be viewed on R**

Then you can move around the codes with the R objects on the list

![GitHub API](/beautiful-jekyll/assets/img/Step 5.png)

**This is a cleaner method if you are only looking for specific r objects in your GitHub API!**
