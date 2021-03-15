---
title: Hexo Commands
date: 2021-03-16 01:41:44
tags:
---

# create post/page/draft
``` bash
hexo new title    # use default_layout setting in _config.yml
hexo new post title
hexo new post "title with space"
hexo new draft "title with space"
```

# publish post from draft
``` bash
hexo pulish "title with space"    #move draft content from source/_drafts to source/_posts folder
```

# blog generation
``` bash
hexo g     # hexo generate
hexo s     # hexo server
hexo s -d  # able to view draft posts
hexo d     # hexo deploy,   publish to github
hexo g -d  # generate and deploy
```

# Reference
* [github flavored markdown syntax](https://docs.github.com/en/github/writing-on-github)
