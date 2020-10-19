[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) [![Netlify Status](https://api.netlify.com/api/v1/badges/686ec137-6a38-4f0b-8717-4ae964b3848c/deploy-status)](https://app.netlify.com/sites/stat545/deploys) [![Build Status](https://travis-ci.com/STAT545-UBC/STAT545-home.svg?branch=master)](https://travis-ci.com/STAT545-UBC/STAT545-home)

**Course as it was at the end of the 2019/2020 academic year, taught by Vincenzo Coia and Firas Moosvi.**

# STAT545-home

Repository that produces the new STAT 545 @ UBC website. Uses Hugo with the Academic theme, wrapped by blogdown, and hosted by netlify. 

## Workflow

This repository is hooked up to Travis CI and Netlify. All you need to do is push a change to the `master` branch, and the site will automatically render and deploy.

Wondering where the `.html` files are? They've been `.gitignore`d, and produced by Travis/Netlify.

## Noteworthy Directory Structure

### `/content`

This is where the content of the website lives. Hugo/blogdown renders this to the `public` folder, which you don't need to touch.

### `config.toml` and `/config`

Website parameters used by Hugo are set in these `toml` files. Check out 

### `/static`

Static stuff like pictures that the site draws on.

### `/history`

I'm using this folder to store historical information about the course, for the hopeful day of putting together some sort of "history" tab in the website.

