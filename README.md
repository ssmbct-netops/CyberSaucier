# CyberSaucier
[![Build Status](https://travis-ci.org/DBHeise/CyberSaucier.svg?branch=master)](https://travis-ci.org/DBHeise/CyberSaucier)
[![dependencies Status](https://david-dm.org/DBHeise/CyberSaucier/status.svg)](https://david-dm.org/DBHeise/CyberSaucier)
[![](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/DBHeise/CyberSaucier/blob/master/LICENSE)

This is a wrapper around [CyberChef](https://github.com/gchq/CyberChef) to allow for programmatic running of recipes.

## API Endpoints
* GET /
    - returns the standard cyberchef.htm (also contained in this repo)
* POST /
    - takes the POST body and runs all available recipes
* POST /{name}
    - takes the POST body and runs the specified recipe
* GET /recipes
    - retrieves a list of available recipes
* GET /recipes/{name}
    - retrieves the specified recipe's JSON data


## Docker image
- available as a docker image, and on dockerhub: [crazydave42/cybersaucier](https://hub.docker.com/r/crazydave42/cybersaucier)


## Configuration - cybersaucier.json
    * Port
        - port on which this will listen (if you change this, you should also make the same change in the Dockerfile)
    * ListenIP
        - IP Address on which to listen
    * DefaultFile
        - file to serve when someone does a basic GET
    * RecipeFolder
        - local folder to store recipes
    * RecipeGit
        - remote git repository where recipes live (can be empty)
    * RecipeGitSparse
        - Sparse getting (only pull the specific folder in the repo) (can be empty)