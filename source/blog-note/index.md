---
title: blog_note
date: 2020-04-28 00:56:35
---

# install hexo
## Step-by-Step
``` bash
npm insntall -g hexo-cli
hexo init <folder>
cd <folder>
npm install
modify _config.yml
git clone https://github.com/theme-next/hexo-theme-next.git themes/next
```

# set deploy to github
1. create <username>.github.io project
2. npm install hexo-deployer-git --save
3. modify _config.yml
``` bash
deploy:
  type: git
  repo: 
    github: git@github.com:<username>/<username>.github.io.git
```
4. then you can check: <username>.github.io


# upload to github for multi-pc synchronization
``` bash 
git init
git checkout -b src
modify .gitignore   #there should have a default one
git add .
git submodule add https://github.com/theme-next/hexo-theme-next.git themes/next
git commit -m "first commit"
git remote add origin git@github.com:wthsieh23/wthsieh23.github.io.git
git push origin src
```

# add SSH public key to github
``` bash
ssh-keygen -t rsa -b 4096 -C "wentsan.hsieh@gmail.com"
ssh-agent -s
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub  # copy the content and paste to github personal setting/ssh
```
