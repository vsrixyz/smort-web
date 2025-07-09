# create-new-revealjs-template

Create a new [Reveal.js](https://github.com/hakimel/reveal.js) presentation from this GitHub Template repository.

* Includes Reveal.js as a **Git submodule** so that Reveal.js's Git commit history is not confused with the presentation's Git commit history.
* Makes future updating of Reveal.js version very easy (see [Updating](#updating-revealjs) below).
* Reduces the size of the presentation repositories significantly.
* Automatically creates update PRs via Dependabot (experimental).
* Scripts included in the `s/` directory for updating the submodule manually, and for creating a PDF version of the slides.

## Usage

1. Click the 'Use This Template' button.

1. Name your presentation repository and it will be created in your own GitHub account/org.

1. Customise as necessary, by cloning locally (or even just using the Github editing UI). See the [Reveal.js documentation](https://revealjs.com/markup/) for information on how to get started with Reveal.js, how to add features, and customise your presentations as necessary.

1. If you clone the repo locally you also need to get the submodule files with `git submodule update --init --recursive`

1. You can use any local server to serve the files. One option is `live-server` (install it with `npm install -g live-server` then type `live-server` in the command line). Using a local server gives you additional features such as live-reload and some of the more advanced [Reveal.js](https://github.com/hakimel/reveal.js) features.

1. Push completed slides back to GitHub

1. Deploy to GitHub Pages (see [GitHub Pages Deployment](#github-pages-deployment) below for detailed steps)

1. **Amaze your friends** by being able to share the URL of your live, interactive slides with your audience immediately. No more emailing PowerPoint attachments for YOU!

## GitHub Pages Deployment

To deploy your presentation to GitHub Pages:

1. **Push your changes** to the main/master branch of your GitHub repository

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click on **Settings** tab
   - Scroll down to **Pages** section in the left sidebar
   - Under **Source**, select **Deploy from a branch**
   - Choose **main** (or **master**) branch
   - Select **/ (root)** as the folder
   - Click **Save**

3. **Wait for deployment:**
   - GitHub will build and deploy your site (usually takes 1-2 minutes)
   - You'll see a green checkmark and URL when ready
   - Your presentation will be available at: `https://yourusername.github.io/repository-name`

4. **Important notes:**
   - Make sure your repository is public (or you have GitHub Pro for private repos)
   - The `index.html` file should be in the root directory (which it is by default)
   - Changes may take a few minutes to appear on the live site
   - You can use a custom domain by adding a `CNAME` file if desired

**Troubleshooting:**
- If slides don't load, check that the submodule was properly initialized with `git submodule update --init --recursive`
- Ensure all file paths in `index.html` are relative (not absolute)
- Check the **Actions** tab in GitHub to see if the deployment succeeded

## Updating Reveal.js

* You may get Dependabot alerts from GitHub to warn you of vulnerabilities in the Reveal.js code. To make these go away, update the submodule.

* To update you can use the script `s/update` which updates Reveal.js to latest. The first time you run this command (on some systems) you will need to make it executable, by running `chmod +x s/update`. This can also be done in the File Manager UI in many systems.

* For older repositories made from this template, the command to run is `git submodule update --rebase --remote`, from the **root** of the repository (not the reveal.js submodule directory itself) to update.

* link for info on updating submodules https://stackoverflow.com/questions/1979167/git-submodule-update

## PDF export of slides

* You can export your slides to PDF using the script `s/pdf`. This will create a PDF file in the root of the repository with the name `slides.pdf`.


## Credits

* [Hakim El-Hattab](https://twitter.com/hakimel) for the simply awesome [Reveal.js](https://github.com/hakimel/reveal.js)
* [Martino Mensio](https://twitter.com/MartinoMensio) for his guide on how to use Reveal.js as a Git submodule in [this](https://martinomensio.medium.com/how-to-host-reveal-js-slides-on-github-pages-and-have-a-tidy-repository-1a363944c38d) blog post (and in doing so I learned how to use and not fear the Submodule!)
* [Excalidraw](https://excalidraw.com/) which is a separate project, mentioned in my presentation template, but I love it so much I wanted to plug it here too.

## License

* MIT Licensed as per Reveal.js itself

## Contributing

* Feel free to make suggestions and PRs to the template repo
