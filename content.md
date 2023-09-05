# Deploying Link in bio to GitHub Pages

(Note: If you previously deployed "Hello, World" to GitHub Pages, then you will see that the instructions here differ slightly. Mainly, we need to rename the repository in this case.)

In the previous lesson you got your "Link in bio" app running in the Codespace live application preview, published the changes to GitHub (commit and push), and got the tests to pass with `rake grade`.

Now it's time to actually deploy that static web site on the internet, so that anyone with the URL can visit it.

To do so, we will use GitHub Pages.

## Rename the repo

This is a special case for GitHub Pages, unlike the "Hello, World" example. We want our images to show up the same way they were in the live application preview when we put them in the `thumbnails/` folder.

In order to get all of the image links to work, the first step to deploying the `<your-username>/links` repo to GitHub Pages is renaming it.

Visit your fork of the repo at `github.com/<your-username>/links` and go to the "Settings" tab.

Under "General", in the field for "Repository name", enter the new name for the repo in the _exact format_:

`USERNAME.github.io`

For instance, my GitHub username in the example below is `bp-demostudent-1`, so my renamed repository is:

`bp-demostudent-1.github.io`


Be sure to actually click "Rename" once you type in the new name:

<!-- ![](/assets/rename-links-to-github-io.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1689120575/rename-links-to-github-io_k6ui15.png)
{: .bleed-full }

## Enable GitHub Pages deployment

Once you rename the repo, find "Pages" in the left sidebar of the "Settings" tab. 

Under "Build and deployment", make sure the "Source" is set to "Deploy from a branch". Under the "Branch", use the dropdown menu to select `main` for the branch and `/(root)` for the location of your files, then click "Save":

<!-- ![](/assets/enable-gh-pages-linkinbio.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1689120585/enable-gh-pages-linkinbio_k0itrn.png)
{: .bleed-full }

## Deploy!

Guess what? Your app is already online (or will be very soon)!

Because we enabled GitHub Pages deployment, anytime you push a commit to GitHub (which you should have done after you created the `index.html` file in your Codespace), your app will be built and deployed to GitHub's free hosting service.

<aside markdown="1">
At first, you may only find the content of the `README` file in the repo at `https://<your-username>.github.io/`. If you don't have an `index.html` file in your repo in the `/(root)` folder, then GitHub Pages treats the `README` as that file and maps your homepage there.

And, how did the page actually deploy? If you visit the "Actions" tab in your code repository, you will see the "pages build and deployment" workflow that ran to deploy the static site. This GitHub Action will be run every time you make changes and publish them to the `main` branch of your repository!
</aside>

Refresh the "Pages" tab in the "Settings" page of your repo after a couple of minutes, and eventually you should see the note "Your site is live at `https://<your-username>.github.io/`":

<!-- ![](/assets/open-github-io-linkinbio.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1689120595/open-github-io-linkinbio_yqpuq8.png)
{: .bleed-full }

If you visit the page by clicking "Visit site" to open in a new tab, you will see your deployed content.

You just built a website that anyone on the internet can visit 🎉

That domain `https://<your-username>.github.io` is provided to you for free by GitHub Pages, and any project repositories with static HTML and CSS that you deploy will be visitable at a URL path on that domain.

In fact, if you previously deployed "Hello, World" on GitHub Pages, then you can still find it at `https://<your-username>.github.io/hello-world`.

You can create as many GitHub Pages sites as you want! 
