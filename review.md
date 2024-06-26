## Git-01-intro

- version control

## Git-02-git-vs-github-vs-gitlab

- manage local project
  - [git](https://git-scm.com/)
- manage online project - team
  - [github](https://gist.github.com/)

## Git-05-git-main-steps

1. working dierctory
2. staging area => مثل برزخ
3. head - repository(repo)

## Git-06-install-git

- in git cmd : `git -v`
- in git cmd : git

## Git-07-git-init

- in project => vscode terminal : `git init` => کنترل پروژه با گیت
- unhide : ctrl + p => >setting => open user setting(json) :

```js
"files.exclude": {
    "**/.git": false,
    "**/.svn": true,
    "**/.hg": true,
    "**/.DS_Store": true
},
```

## Git-08-add-file-to-stage

- command_1 : `git status`
  - U : untract => به مرحله استیج نرفته
- command_2 : `git add fileName` --- `git add .`
  - A : staging Area
  - M : modify

## Git-09-remove-file-from-stage

- commnad : `git -rm --cached fileName`

## Git-10-git-commit => send to repo

- commannd : `git commit -m 'meeage'`
- we should add & commit after each change

## Git-11-git-log

- command_1 : `git log` => information about commits
- command_2 : `git log --oneline` => summerize commits
- command_3 : `git log --oneline --all`

## Git-12-git-log-flags

- command_1 : `git log --stat` => امار دقیق تر کامیت ها
- command_2 : `git log --graph` => نموداری بودن کامیت ها
- command_3 : `git log --after="23-10-12"`=> فیلتر کردن کامیت ها
- command_4 : `git log --before="23-10-12"` => فیلتر کردن کامیت ها
- command_5 : `git log --author="userName"` => فیلتر کردن کامیت ها

## Git-13-am-commit-flag

- command : `git commit -am "message"` => add + commit

## Git-14-git-show

- command_3 : `git show commitID fileName`
- command_1 : `git show commitID`
- command_2 : `git show` => last commit

## Git-15-git-alias

- command :`git config --local alias.lgo "log --oneline"`
- command : `git config --global alias.lgo "log --oneline"`
- .git => config => you can see ailas

## Git-16-what-is-branch

## Git-17-create-and-switch-on-branch

- command_1 : `git branch` => currently branch
- command_2 : `git branch nameOfBanch` => create branch
- command_3 : `git switch nameOfBanch`
- command_4 : `git switch -c nameOfBanch` => create + switch

## Git-18-remove-branch

- command_1 : `git branch -d nameOfBanch`
- command_2 : `git branch -D nameOfBanchc` => branch with changes

## Git-19-rename-branch

1. switch to branch
2. rename branch name

- command : `git branch -m newBranchName`

## Git-20-gitlens-extension

## Git-21-git-fast-forward-merge

1. fast forward
   1. in master branch
   2. command : `git merge branchName`
2. Non fast-forward

## Git-22-git-non-fast-forward-merge-01

2. Non fast-forward
   1. in master branch
   2. command : `git merge branchName`
   3. write message

## Git-23-git-non-fast-forward-merge-02

2. Non fast-forward with `conflict`
   1. in master branch
   2. command : `git merge branchName`
   3. solve conflict
   4. `git add .`
   5. `git commit -m message`

## Git-24-merge-best-practice

- each branch each feature

## Git-25-semantic-commit-messages

- [semantic-commit-messages-1](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)
- [semantic-commit-messages-2](https://www.conventionalcommits.org/en/v1.0.0/)

## Git-26-git-diff

- compare between two commit or two branch
- command : `git diff` => compare working diectory & staging area

## Git-27-git-diff-stage

- command : `git diff --staged` => compare last commit & staging area

## Git-28-git-diff-head

- head = master
- command : `git diff head`---`git diff HEAD` => comparelast commit & working diectory

## Git-29-compare-commits-or-branches

- compare commits :
  - command_1 : `git diff commit_1_ID..commit_2_ID `
  - command_2 : `git diff commit_1_ID..commit_2_ID  fileName`
- compare commits in different branches :
  - command_1 : `git diff master branchName`

## Git-30-gitignore

1. create .gitignore file next to .git folder
2. write file names in previous file
3. add and commit change

- [gitignore](https://www.gitignore.io/)

## Git-31-checkout

- return to before commits

  - command_1 : `git checkout commitID`
    - کامیت های بعدی از بین میرود
  - command_2 : `git checkout commitID fileName`
    - کامیت های بعدی ان فایل از بین میرود
  - command_3 : `git checkout HEAD~3`

- برگشت تنظیمات :
  - command_1 : `git switch master`

## Git-32-discard-wd-changes

- remove changes in working directory
  - command_1 : `git checkout HEAD fileName`
  - command_2 : `git checkout HEAD .`

## Git-33-git-restore-01

- discard-wd-changes => حذف تغییرات در دایرکتوری خودمان
  - command : `git restore fileName`
- unstage file => ببر به قبل ادد
  - command : `git restore --staged fileName`

## Git-34-git-restore-02

- return to before commits => برگشت به کامیت های قبلی
  - command_1 : `git restore --source commitID fileName`
  - command_2 : `git restore --source HEAD fileName`
  - command_3 : `git restore --source HEAD~3 fileName`

## Git-35-git-clean

- delete files
  - commamd_1 : `git clean fileName`
  - commamd_2 : `git clean -h` => راهنمای حذف کردن
  - commamd_3 : `git clean -f -d fileName`

## Git-36-git-reset-concept

- کامند خطرناک 😂
- reset :

  1. Soft => for commit history (Repo)

     - command : `git reset --soft`

  2. Medium => for add and commit history (Stage & Repo)

     - defualt command
     - command : `git reset --mixed`

  3. Hard => for 3 level (Wd & Stage & Repo)
     - command : `git reset --hard`

## Git-37-soft-reset

- command : `git reset --soft  commitID`
- we cant recovery => return canges to stage

## Git-38-def-and-hard-reset

1.

- command : `git reset --mixed  commitID`
- return canges to wd

2.

- ترکاندن کامیت و ..
- command : `git reset --hard commitID`
- untracted files dont change

## Git-39-revert-in-git

- از بین بردن کامیت و خنثی کردن تغییرات
- like `git reset --hard`
- command : `git revert commitID`
- use vscode : `ctrl + p` => `>GitLence:revert` => choose commit
- use commit message

## Git-40-conflict-in-revert

## Git-41-git-status-short

- command_1 : `git status -h` => help
- command_2 : `git status -s` => short

## Git-44-git-clone

- command : `git clone repositoryName`

## Git-47-git-remote

- command_1 : `git remote` => چک میکند که ایا پروژه به گیت هاب یا گیت لبی متصب بوده یا نه
  - origin => اسم ریموت دیفالت
- command_2 : `git remote add remoteName ref` => وصل کردن پروژه به یک ریموت
- command_3 : `git remote -v` => اطلاعات بیشتری در مورد ریموت
- command_4 : `git remove remoteName(origin)` => حذف کردن ریموت

## Git-48-git-push

- command_1 : `git push origin main`
- command_2 : `git push -u origin main`

## Git-49-git-pull

- bring others changes from to local repository
- command_1 : `git pull`

## Git-50-git-fetch

- like pull but don't merge commits => `git pull` = `git fetch ` && `git merge`
- command_1 : `git fetch <remote> <branch>`
- command_2 : `git branch -r` => دیدن ریموت برنچ ها
- command_3 :`git switch -c seeChanges origin/master` => دیدن تغییرات در یک برنچ دیگر
- commad_4 : `git merge seeChange`
- commad_5 : `git branch -d seeChange `

## Git-51-remote-branch

## Git-52-learn-deeply

![learn-deeply](/assets/learn-deeply.png)

## Git-53-pull-with-conflict

- command_1 : `git pull` => like before

## Git-54-readme-and-markdown

- [markdown_1](https://markdown-it.github.io/)
- [markdown_2](https://www.markdownguide.org/)

## Git-55-link-and-img-in-readme

## Git-56-badge-in-readme

![npm downloads](https://img.shields.io/npm/dw/express)
![ downloads](https://img.shields.io/npm/dw/cors)

- [Badges4-README.md-Profile :](https://github.com/alexandresanlim/Badges4-README.md-Profile)

  - ![gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)

## Git-57-readme-so

- [quick readme](https://readme.so/)

## Git-58-github-page

[github-page](https://pages.github.com/)

1. create new repository

2. `git clone repository`

3. create file `index.html`

4. setting => page => master root

- how to deploy react app on github ?
  - [deploy react app](https://www.youtube.com/watch?v=Q9n2mLqXFpU)

## Git-59-private-repo

## Git-60-invite-collaborator

## Git-61-issues

- Git-issues : ارتباط افراد با یک دیگر
  - mention sb
  - tag labels

## Git-62-issues-in-teams

- issues-in-teams : مشخص کردن تسک هر کس

  - اسم ان فرد را باید منشن کنیم

- how save changes in issues :

  1. `git add .`

  2. `git commit -m "commitMessage - resolve #issueId"` => خود به خود کلوز میشود

  3. `git push`

## Git-63-pull-request-in-team

1. `git branch` => master
2. `git swich -c "branchName"`
3. make your changes
4. `git add .`
5. `git commit -m "commitMessage"`
6. `git push`
7. `git push --set-upstream origin branchName`

## Git-64-pull-request-with-conflict

- how to merge :
  - resolve conflict options

## Git-65-fork

- copy other `s repository and add to our repository and we can pull requests changes to them

## Git-66-push-on-forked-repo & Git-67-pull-req-on-forked-repo

- we can change our repository posibilty (private to public and reverse)

1. like before sessions
2. click contribute to pull reguest to target

## Git-68-pull-from-main-repo

- زمانی که در ریپو اصلی تغییر ایجاد شود

1. ‍‍`git remot add upstream mainRef`

2. `git remore -v`

3. `git pull upstream main`

## Git-73-shields-io

- [badges](https://shields.io/)
- [markdown-badges](https://github.com/Ileriayo/markdown-badges)
- [icon](https://icons8.com/)
- [icon](https://skillicons.dev/)

## Git-74-add-readme-to-profile

- create a repository with your github username

## Git-75-github-stats

- [برای استفاده آمار و ارقام اکانت گیت هاب ](https://github.com/anuraghazra/github-readme-stats)

# Git-76-markdown-pro-tips

- [bold in markdown](https://www.markdownguide.org/basic-syntax/#bold)

- [italic in markdown](https://www.markdownguide.org/basic-syntax/#italic)

- [horizontal line in markdown](https://www.markdownguide.org/basic-syntax/#horizontal-rules)

- [blockquotes in markdown](https://www.markdownguide.org/basic-syntax/#blockquotes-1)

- [diff codes in markdown](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks)

```diff
 {
-"firstName": "John",
 "lastName": "Smith",
  "age": 25
}
 {
+ "firstName": "Joo",
  "lastName": "Smith",
  "age": 25
}
```

- [list in markdown](https://www.markdownguide.org/basic-syntax/#lists-1)

- [table in markadown](https://www.markdownguide.org/extended-syntax/#tables)

## Git-83-achievements

- github-achievements => دستاورد های گیت هاب
- [github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy)
- [Get-Github-Achievements](https://github.com/4xmen/Get-Github-Achievements)

## Git-84-code-inprofile

```js
const thai = {
  pronouns: "She" | "her",
  langs: [Javascript, Typescript, HTML, CSS],
  tools: [
    React,
    Redux,
    Node,
    Next,
    Tailwind,
    Storybook,
    Styled - Components,
    Jest,
    Docker,
  ],
  architecture: ["Microservices", "event-driven", "design system pattern"],
  techCommunities: {
    coorganizer: "AfroPython",
    speaker: "Latinity",
    mentor: "EducaTRANSforma",
  },
  challenge:
    "I am doing the #100DaysOfCode challenge focused on react and typescript",
};
```


