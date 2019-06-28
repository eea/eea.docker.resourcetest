# Docker image for resource count checker

## Supported tags and respective `Dockerfile` links

- [`latest` (*Dockerfile*)](https://github.com/eea/eea.docker.resourcetest/blob/master/Dockerfile)
- [`0.1` (*Dockerfile*)](https://github.com/eea/eea.docker.resourcetest/blob/0.1/Dockerfile)

## Usage

    $ docker run -it --rm -e JS_ORG="" -e CSS_ORG="" -e REG_URL="" eeacms/resourcetest

## Running in jenkins, including pull requests:

* GIT_NAME, GIT_SRC  - must be given
* GIT_BRANCH - defaults to master
* GIT_CHANGE_ID - can be empty or pull request id
* JS_ORG, CSS_ORG - the number of resources to check against
* REG_URL - the url that you want to test

    $ docker run -i --rm -e GIT_SRC="https://github.com/eea/$GIT_NAME.git" -e GIT_NAME="$GIT_NAME" -e GIT_BRANCH="$BRANCH_NAME" -e GIT_CHANGE_ID="$CHANGE_ID" -e JS_ORG="" -e CSS_ORG="" -e REG_URL=""  eeacms/resourcetest
