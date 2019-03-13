[![CircleCI](https://circleci.com/gh/gnuton/circleci-template.svg?style=svg)](https://circleci.com/gh/gnuton/circleci-template)

# Circleci-template
Every branch of this repository contains different CI pipelines for circleCI.

## wait-for-approval branch
the .circleci dir in this branch contains the following workflow

  BUILD --> WAIT FOR APPROVAL --> PUBLISH RELEASE on GITHUB

So basically you release your code using the circle ci web interface, just by clicking the "approve" button.
Please note that if the two or more releases with the same version are uploaded to github, the lastes overwrite the previous.

## tag-for-release branch
the .circleci dir in this branch contains the following workflow
 BUILD --> PUBLISH RELEASE on GITHUB

The build steps runs everytime, but the publish one happens only when we push a tag like 1.0.0.
```bash
git tag 0.0.1
git push --tag
# circleCI will build again and push the release to github
```
