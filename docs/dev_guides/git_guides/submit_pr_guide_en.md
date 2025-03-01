# Guide of submitting PR to Github

## Finish Pull Request create PR

Create an Issue to describe your problem and keep its number.

Switch to the branch you have created and click `Compare & pull request`。

![new_pull_request](../images/compare_pull_request.png)

Switch to targeted branch:

![change_base](../images/change_base.png)

If the issue of an Issue is resolved, please add: fix #issue_number to the first comment box of the PUll Request, so that when the PUll Request is merged, the corresponding Issue will be automatically closed. Keywords include: close, closes, closed, fix, fixes, fixed, resolve, resolves, resolved, please choose the appropriate word. For details, please refer to

Then please wait for review.If there is any need to make a modification,you can update corresponding branch in origin following the steps above.


## Sign CLA and pass unit tests

### Sign CLA

For the first time to submit Pull Request,you need to sign CLA(Contributor License Agreement) to ensure merge of your code.Specific steps are listed as follows:

- Please check the Check in PR to find license/cla and click detail on the right to change into CLA website.

<div align="center">

<img src="https://github.com/PaddlePaddle/FluidDoc/blob/release/1.1/doc/fluid/advanced_usage/development/contribute_to_paddle/img/cla_unsigned.png?raw=true"  height="40" width="500">

 </div>

- Please click “Sign in with GitHub to agree” in CLA website.It will change into your Pull Request page after the click.

<div align="center">

<img src="https://github.com/PaddlePaddle/FluidDoc/blob/release/1.1/doc/fluid/advanced_usage/development/contribute_to_paddle/img/sign_cla.png?raw=true"  height="330" width="400">

 </div>


### Pass unit tests

Every new commit in your Pull Request will trigger CI unit tests,so please make sure that necessary comments have been included in your commit message.Please refer to [commit](./local_dev_guide_cn.html#commit)

Please note the procedure of CI unit tests in your Pull Request which will be finished in several hours.

Green ticks after all tests means that your commit has passed all unit tests,you only need to focus on showing the Required tasks, the ones not showing may be the tasks we are testing.

Red cross after the tests means your commit hasn't passed certain unit test.Please click detail to view bug details and make a screenshot of bug,then add it as a comment in your Pull Request.Our stuff will help you check it.


## Delete remote branch

We can delete branches of remote repository in PR page after your PR is successfully merged into master repository.

![delete_branch](../guides/10_contribution/img/delete_branch.png)

We can also delete the branch of remote repository with `git push origin :the_branch_name`,such as:

```bash
➜  git push origin :my-cool-stuff
```

## Delete local branch

Finally,we delete local branch

```bash
# Switch to develop branch
➜  git checkout develop
# delete my-cool-stuff branch
➜  git branch -D my-cool-stuff
```

And now we finish a full process of code contribution
