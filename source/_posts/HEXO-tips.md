---
title: HEXO使用心得
copyright: true
date: 2019-05-29 21:02:04
tags: blog
password: loveyouxyn
abstract: Welcome to my blog, enter password to read.
message: Welcome to my blog, enter password to read.
---

# HEXO加密

F:\Blog\themes\hexo-theme-sagiri\layout\_partials\head.swig

低级加密：

```javascript
<script>
    (function(){
        if('{{ page.password }}'){
            if (prompt('请输入文章密码') !== '{{ page.password }}'){
                alert('密码错误！');
                history.back();
            }
        }
    })();
</script>
```

高级加密：

npm install --save hexo-blog-encrypt



# HEXO-APLAYER开关

blog下config

主题source下dist下

主题layout下_layout.swig