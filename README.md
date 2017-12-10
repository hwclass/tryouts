### Node development environments with Docker & git flow

#### Git flow

**Create repo**
* Create directory and git init
* git remote add origin git@github.com:hwclass/docker-tryouts.git
* git checkout -b develop & git push

**Create foo feature branch**
* git checkout -b feature/foo develop
* vim foo.js
* git add foo.js
* git commit -m "New feature file added, foo.js"
* git push

**Create bar feature branch**
* git checkout -b feature/bar develop
* vim bar.js
* git add bar.js
* git commit -m "New feature file added, foo.js"
* git push

**Merge foo feature into develop**
* git checkout develop
* git merge feature/foo
* git push

**Rebase foo feature with develop branch**
* git checkout feature/foo
* git rebase develop

**Merge bar feature into develop**
* git checkout develop
* git merge feature/bar
* git push

**Rebase bar feature with develop branch**
* git checkout feature/bar
* git rebase develop

**Create release branch and send**
* git checkout -b release/1.0 develop
* Edit foo and git add & git push -u origin release/1.0

**Merge release branch into develop with changes**
* git checkout develop
* git merge release/1.0
* git push

**Merge release branch into master with changes and tag it**
* git checkout master
* git merge release/1.0
* git push
* git tag v1.0.0
* git push origin v1.0.0

**Hotfix from master**
* git checkout master
* git checkout -b hotfix/fix-foo
* git commit -m "Single foo after all"
* git checkout master
* git merge hotfix/fix-foo
* git push
* git tag v1.0.1
* git push origin v1.0.1
* git checkout develop
* git merge hotfix/fix-foo
* git push

**Clean after development and merging**
* git branch -d feature/foo
* git branch -d feature/bar
* git branch -d hotfix/fix-foo
* git checkout
logs:
  develop
* master
  release/1.0




