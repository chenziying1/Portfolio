## 运行命令

bundle exec jekyll serve

前提条件是将_config.yml中的 baseurl: ""设置为这样，baseurl: "/Portfolio"是用于github部署

## 修改模板

我们使用的是minima，这也是支持github部署的模板之一

如果想要修改minima模板内容，就得复制原本的过来（bundle show minima看路径）过来，然后修改，运行bundle exec jekyll serve

*我们的在这里：F:\Ruby34-x64\lib\ruby\gems\3.4.0\gems\minima-2.5.1

*bundle show minima查看当前使用哪一个版本的minima和路径
