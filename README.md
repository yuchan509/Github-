# Github
Git 사용법

- **Step0.**
  - git config --global user.email 'my email'
  - git config --global user.name 'my name'

- **Step1.**
  - git clone 'URL' '폴더명'
    
- **Step2. Clone repasitory**
  - git init

- **Step3. Change branch**
  - git branch -M main

- **Step4. Check status**
   - git status

- **Step5. Commit**
  - git add *
  - git commit -m 'My Git File Name'

- **Step6. Remote**
  - git remote add origin 'My Git URL'

- **Step7. Pull**
  - git pull --rebase origin main

- **Step8 Push**
  - git push origin main

- **Step9 Delete**
  - git rm -r - cached '파일명/폴더명' 
  - git commit -m 'delete 파일명/폴더명'
  - git push origin main(branch명)
