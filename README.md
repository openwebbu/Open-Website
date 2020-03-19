<p align="center">
	<img width="200" src="assets/img/logo.svg" alt="open-web">
</p>

# Open Website

All of the code for the Open Web website lives here now. Check it out, and feel free to use this as a starting point for your own website! 

## Repo Overview

We use [Hugo](https://gohugo.io/getting-started/installing/) to build our site, and [npm](https://www.npmjs.com/get-npm) to manage all of our dependencies. You will need to install both of those in orderr to build and run the website on your own computer. 

Quick outline of the directory structure: 

* `archetypes` contains files that describe to Hugo how to initilize new files that are created with hugo new. 
* `assets` contains files that are going to be processed and output in static/ for Hugo to copy directly.
    * Notably, the main sass and typescript for the site is here
* `content` is where all of the site's content and images go to be processed by Hugo
* `docs` is where the built final output goes to be served with Github Pages
* `layouts` is where files that describe to Hugo how it needs to generate types of pages go. 



* Assets contains the js and css for the whole site
    * Images linked in css will get linked automatically in static, so at the moment you don't need to copy anything into static yourself (not sure about html though)
    
## Running the Website

If you just want to add pages, then put some new stuff in Content. Look at other files for references in how to include images, icons, and more. 

* run `npm install` to install all the dependencies of the project.
    * **You will need to change a variable in `node_modules/@fortawesome/fontawesome-free/scss/_variables`**: `$fa-font-path` should be `"../node_modules/@fortawesome/fontawesome-free/webfonts" !default;`, not `"../webfonts" !default;`
* run `npm run start` for quickly working on the site as that shows your edits to pages live. It does not regenerate the styles or javascript automatically though, so if you need to edit that run the command again. 
* run `npm run build` when you're ready to commit back up to the website (or if serve is being weird). Somestimes start will change more files in docs than necessary, but build ensures you only commit what's necessary.
