[![CircleCI](https://circleci.com/gh/gnuton/circleci-template.svg?style=svg)](https://circleci.com/gh/gnuton/circleci-template)

# Circleci-template
This repository contains all circleCI files required to build some common pipelines:

## Master branch
the .circleci dir in the master branch contains this workflow

  BUILD --> WAIT FOR APPROVAL --> PUBLISH RELEASE on GITHUB

So basically you release your code using the circle ci web interface, just by clicking the "approve" button.
Please note that if the two or more releases with the same version are uploaded to github, the lastes overwrite the previous.
