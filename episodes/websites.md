---
title: "Hosting websites on GitHub Pages"
teaching: 30
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions

- How do I serve a website using GitHub?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Enable GitHub Pages for a repository
- Watch GitHub build and deploy a page using GitHub Actions
- View the resulting website

::::::::::::::::::::::::::::::::::::::::::::::::

You can host your personal homepage or group webpage or project website on
GitHub using [GitHub Pages](https://pages.github.com/).

[GitLab](https://about.gitlab.com/features/pages/) and
[Bitbucket](https://confluence.atlassian.com/bitbucket/publishing-a-website-on-bitbucket-cloud-221449776.html)
also offer a very similar solution.

Unless you need user authentication or a sophisticated database behind your
website, [GitHub Pages](https://pages.github.com/) can be a very nice
alternative to running your own web servers.

## Step 0: Add links to your recipes in README.md

*(This is from Step 3 of [Making changes with GitHub Desktop](gh-desktop-changes.md),
so you may have already done this)*

Go back to your initial recipes repository, and edit your README.md file so
that you have links to your separate recipe markdown files.

Here is sample text to include:

```
# Avocado Recipes
A collection of my avocado recipes

* [Smoothie](avocado_smoothie.md)
* [Guacamole](guacamole.md)
* [Salad](avocado_tomato_salad.md)

```

Commit these changes.

## Step 1: Tell GitHub to make your pages

We need to tell GitHub how to make your repository into a website.

Click on the Settings gear icon up top, and then click on the Pages section
on the left side panel.

![A screenshot showing the GitHub Settings Page section](fig/settings_pages.jpg){alt='Screenshot showing the GitHub Settings Pages section'}

Click on the dropdown under Branch, and select "main" to tell GitHub to
build a webpage from the "main" branch. Then make sure that "/root" is
selected in the new dropdown that will populate. Click Save to make the web
page build.

![A screenshot showing the GitHub Settings Page section, with main branch and root selected](fig/settings_main_root.jpg){alt='Screenshot showing the GitHub Pages settings with the main branch and root folder selected'}

## Step 2: Watch GitHub build your page live

Right after clicking Save, GitHub will start building your page using
GitHub Actions (we could do a whole extra workshop on GitHub Actions).

Click on the Actions icon on the top menu to see that a "workflow" has been
triggered called "pages build and deployment".

![A screenshot showing the GitHub Actions page with a deployment that has just been triggered](fig/github_actions_workflows.jpg){alt='Screenshot of the GitHub Actions page showing a pages build and deployment workflow that was just triggered'}

If you clicked on the Actions tab fast enough, the circle next to the
workflow name should be brown or yellow.

Click on the "pages build and deployment" link. If the build was successful,
all parts of the workflow should show a green circle. And most importantly,
the "deploy" portion should have a link to your new website!

![A screenshot showing details of a GitHub Actions workflow](fig/github_actions_built.jpg){alt='Screenshot of a completed GitHub Actions workflow with a link to the deployed site'}

Click on that link (it should follow the pattern
`https://[your username].github.io/recipes`). You should see a pretty basic
webpage, but it's completely built from the contents of your GitHub
repository!

![A screenshot showing a simple webpage with links to recipes](fig/webpage.jpg){alt='Screenshot of a simple deployed webpage with links to recipes'}

::::::::::::::::::::::::::::::::::::: keypoints

- GitHub Pages can turn the contents of a repository into a live website.
- Enabling Pages triggers a GitHub Actions workflow that builds and deploys
  the site.
- The deployed site's URL follows the pattern
  `https://[your username].github.io/[repository name]`.

::::::::::::::::::::::::::::::::::::::::::::::::
