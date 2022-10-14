基于cookiecutter创建 Markdown latex Article 模版
================

依赖
------------

- cookiecutter 
- pandoc
  
cookiecutter和pandoc都需要由此生成输出文件
模板。第一个工具将使您能够轻松地添加不同的项目数据
这样的标题、副标题、作者等。第一个工具可以操作md文件生成latex文档。

使用
---
安装 cookiecutter 并设置项目： 

```bash
pip install cookiecutter
cookiecutter https://github.com/llango/cookiecutter-md-article -f -o ..
```

下一步
-----

- [ ] 完善文章模版。
- [ ] 修改字体是的文章模版更为专业。