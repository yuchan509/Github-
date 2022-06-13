# Github
Git 사용법

- **Step0.**
  - `git config --global user.email 'my email'`
  - `git config --global user.name 'my name'`

- **Step1.**
  - `git clone 'URL' '폴더명'`
    
- **Step2. Clone repasitory**
  - `git init`

- **Step3. Change branch**
  - `git branch -M main`

- **Step4. Check status**
   - `git status`

- **Step5. Commit**
  - `git add *`
  - `git commit -m 'My Git File Name'`

- **Step6. Remote**
  - `git remote add origin 'My Git URL'`

- **Step7. Pull**
  - `git pull --rebase origin main`

- **Step8 Push**
  - `git push origin main`

- **Step9 Delete**
  - `git rm -r - cached '파일명/폴더명'` 
  - `git commit -m 'delete 파일명/폴더명'`
  - `git push origin main(branch명)`

- **Step10 git Manipulation**
  - `git log` : 해당 repo의 git log들을 보여줌.
  <br>
  
  ```git
  Owner@DESKTOP-72245DQ MINGW64 ~/Desktop/Data-Collection (main)

  $ git log
  commit (e4d003c14c76e1b7f46b97f5e26e265ce33d3665 : Hash Value) (HEAD -> main, origin/main, origin/HEAD)
  Author: Yuchan <75283773+yuchan509@users.noreply.github.com>
  Date:   Mon Apr 18 12:00:00 2022 +0000

    Update README.md

  commit 6a762c03efb297a9e74df8ce8db3640bd6b49ede
  Author: Yuchan <75283773+yuchan509@users.noreply.github.com>
  Date:   Thu Mar 10 12:00:00 2022 +0000
  
  ....ing
  ```

  - `Git rebase -i Hash Value` : e4d003c14c76e1b7f46b97f5e26e265ce33d3665
    - 수정하고 싶은 date를 선택하여 pick -> edit으로 전환.
    - "i" key를 통해 command mode -> insert mode로 변환하며 pick에서 edit으로 수정이 가능.
    - 변경이 끝난 후, ESC key + :wq! 를 통해 해당 작업 종료.
    
   <br>

  ```git
  pick (-> edit) 6a762c0 Data Collection
  pick e4d003c Update README.md

  # Rebase bae1533..e4d003c onto bae1533 (2 commands)
  #
  # Commands:
  # p, pick <commit> = use commit
  # r, reword <commit> = use commit, but edit the commit message
  # e, edit <commit> = use commit, but stop for amending
  # s, squash <commit> = use commit, but meld into previous commit
  # f, fixup [-C | -c] <commit> = like "squash" but keep only the previous
  #                    commit's log message, unless -C is used, in which case
  #                    keep only this commit's message; -c is same as -C but
  #                    opens the editor
  # x, exec <command> = run command (the rest of the line) using shell
  # b, break = stop here (continue rebase later with 'git rebase --continue')
  # d, drop <commit> = remove commit
  # l, label <label> = label current HEAD with a name
  # t, reset <label> = reset HEAD to a label
  # m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
  # .       create a merge commit using the original merge commit's
  # .       message (or the oneline, if no original merge commit was

  ```
  
  - `git commit amend` : 원하는 date로의 수정이 가능
  - e.g) git commit --amend --no-edit --date="{date}"
    - input : git commit --amend --no-edit --date="JAN 01 12:00:00 2022 +0000"


  - `git rebase --continue` : rebas 완료.

  - `git push -f origin main` : 수정한 내용 push.


- Step11. Edit commit message
- [Reference](https://github.com/yuchan509/Frontend-Study)
