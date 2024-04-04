# hugo-mock-landing-page

CIS 3500 Software Engineering: [Homework 2](https://cis-3500.github.io/docs/example/homeworks/homework-2)

Part II Instructions: [Automating the Deployment of a Hugo Website \(hugo-mock-landing-page-autodeployed\)](https://cis-3500.github.io/docs/example/homeworks/homework-2/#part-ii-automating-the-deployment-of-a-hugo-website-hugo-mock-landing-page-autodeployed)

I've set up a workflow using GitHub Actions that helps me automatically update my Hugo website on GitHub Pages every time I make changes and push them to the `main` branch.

- The workflow fetches the repository: When I push updates, the workflow starts by grabbing the latest code from my repository.
- The workflow initializes the Hugo environment: Hugo is the tool I use to turn my content into a static website. The workflow sets up Hugo with the exact settings I need, like the specific version and whether I'm using the extended version, ensuring Hugo is ready to build my site just the way it should be.
- The workflow builds the static site: The workflow compiles the Hugo site, generating static HTML files from the content and theme. It includes flags to delete unused files (`--gc`), include drafts in the build (`-D`), and minimize output size (`--minify`).
- The workflow publishes it to GitHub Pages: The last step is where the magic happens! The workflow takes the static site Hugo built and puts it on my GitHub Pages site, specifically on a branch called `gh-pages`. It handles logging in for me and makes sure the update is done correctly, with all changes coming from a bot account, so it's clear it was an automated update!

My published site: https://kimttfung.github.io/hugo-mock-landing-page-autodeployed/


![preview](static/images/site-preview.png)