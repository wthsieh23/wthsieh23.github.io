---
title: My First Blog
date: 2020-05-01 08:01:10
categories:
- blog
tags:
- hexo
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
4. then you can check: username.github.io


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

# add categories
``` bash
hexo new page categories
```

then add type in `source/categories/index.md`
``` 
---
title: categories
date: 2020-05-01 06:45:20
type: "categories"
---
```

then add the below attributes in the page you want
``` bash
---
title: xxx
categories:
- test      # category
- test1     # subcategory
---
```

# add tags
``` bash
hexo new page tags
```

add type in `source/tags/index.md`
```
---
title: tags
date: 2020-05-01 07:04:55
type: "tags"
---
```


then add tags as below in the page you want
```
---
title: tags
date: 2020-05-01 07:04:55
type: "tags"
---
```

# local search
install the package
`npm install hexo-generator-searchdb --save`

enable the local search feature in `themes/next/_config.yml`
```
# Local Search
# Dependencies: https://github.com/theme-next/hexo-generator-searchdb
local_search:
  enable: true
```

add below content to blog's `_config.yml`
```
search:
  path: search.json
  field: post
  content: true
  format: html
  limit: 10000
```
