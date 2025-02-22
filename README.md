# Upload local git repo to github
### A step-by-step tutorial to creating a replica of a local git repo on github 

## The scenario
Assume that you have a local git repo with multiple branches. If you're willing to make an exact replica of this repo follow these steps:


1) Manually create a GitHub repo of any name
2) On your local repo, checkout to each single branch and execute the following commands:
```bash
git config set push.default current
git config --bool set push.autoSetupRemote true
git push
```

> `git config set push.default current` sets the current branch to update a remote branch with the same name
> `git config --bool set push.autoSetupRemote true` enables the `push` command to automatically read push configuration from `push.default`
