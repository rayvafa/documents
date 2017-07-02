# Software development principles

## Github
* We use Github as version control
* we use Gitflow as a principle: http://nvie.com/posts/a-successful-git-branching-model/
* You shouldn't directly commit any code to develop or master branch
* You should open Pull Request to merge your code in develop branch
* Your code needs to get approval and build successfully in order for it to get merge 
* The job is done only if the PR is merged

## Javascript code style and linter
* We use Airbnb style guide: https://github.com/airbnb/javascript
* We use ESlint for enforcing the style guide
* We use CircleCI for build process ( running lints and test units )
* All lint issues should be resolved before code review
