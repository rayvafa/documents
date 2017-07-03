# Software development principles

## Requirements and best practices
* All the UI should be built mobile first
* Use SVG instead of png or jpg whenever possible

## Javascript code style and linter
* We use Airbnb style guide: https://github.com/airbnb/javascript
* We use ESlint for enforcing the style guide
* We use CircleCI for build process ( running lints and test units )
* All lint issues should be resolved before code review

## Github
* We use Github as version control
* we use Gitflow as a principle: http://nvie.com/posts/a-successful-git-branching-model/
* You shouldn't directly commit any code to develop or master branch
* You should open Pull Request to merge your code in develop branch
* Your code needs to get approval and build successfully in order for it to get merge 
* The job is done only if the PR is merged

## Why PRs? Why individual commits?

A general rule of thumb:
If you create a PR that has 3 headings describing different changes,
that would imply these changes would ideally be 3 separate PRs.

You should keep your PRs and your commits _[atomic](https://www.freshconsulting.com/atomic-commits/)_:

> ### Atomic Approach
> 
> - Commit each fix or task as a separate change
> - Only commit when a block of work is complete
> - Commit each layout change separately
> - Joint commit for \[JSX and CSS changes\], and additional resources
> 
> ### Benefits
> 
> - Easy to roll back without affecting other changes
> - Easy to make other changes on the fly
> - Easy to merge features to other branches

Then, each PR is a set of commits related to one change or task.
Sometimes, this means a single commit per PR.
Other times, it means many commits for a PR.

## Making a pull request

### Branching out

Before submitting a PR make sure that you're on a fresh branch that's named after the work that you're doing

### Committing your changes

Commit your changes with descriptive messages. 

### Test and lint

Run `yarn run test` to check for any linting or test errors and make sure they're all fixed.
CI should catch these once you submit the PR, but it's good to catch them early.

## CircleCI

Why?
Circle will run `yarn test` and `yarn lint` for your repo every time you push to GitHub and the results will be shown in the GitHub UI. It will help us maintain code quality and restrict us merging branches that fail tests.
