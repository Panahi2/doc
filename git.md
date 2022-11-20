# قبل از هز کاری چک شود
```
git pull
git branch
```

# Gitlab
- Run Unit Test
- Run build

# Install Gitlab
- about.gitlab.com/install/#ubuntu
- about.gitlab.com/ee/update/package/#upgrade-using-a-manualy-download-package
- packages.gitlab.com/gitlab/gitlab-ce
- download focal -> amd64
- sudo apt-get install gitlab-ce
- sudo dpkg -i gitlab
### show password stdout
- GITLAB_ROOT_PASSWORD
- /etc/gitlab/initial-root-password
### Domain
- EXTERNAL_URL="http://gitlab.local
- /etc/gitlab/gitlab.rb
- sudo gitlab-ctl reconfigure

- sudo gitlab-ctl status
- sudo gitlab rails console
- user=user.find_by_username 'root'
- user.password=''
- user.passwordconfirmation=''
- user.save!
- exit

# Git
- change address Submodule in git: `git mv old/submod new/submod`
- stage diff: `git diff --cached`
- remove submodule: `git rm <path-to-submodule>`
- show which specific files are ignored by .gitignore: `git status --ignored`
- Force add despite the .gitignore file: `git add --force my/ignore/file.foo`
- when use submodule: https://www.atlassian.com/git/articles/core-concept-workflows-and-tips


# Add Remote
```
git remote add origin url
git remote -v
git push --set-upstream origin master
git branch -m main // Rename branch master to main
```

# Uncommited changes into another branch
- git stash
- git checkout branch2
- git stash pop

# حذف ‌branch از remote
- git push origin --delete branch

# Merge Branches
merge branch2 to branch1
- git merge --no-ff branche2

# Submodule
- git submodule update --init --recursive
- git pull --recursive
- git submodule foreach --recursive git fetch
- git submodule foreach git merge origin master
