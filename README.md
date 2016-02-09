# hexo-theme-raytaylorism v2

raytaylorism（Ray Taylor主义）是我自己设计并制作的一款清新的的响应式Material Design风格的[Hexo]主题。该主题支持最新的Hexo 3.1版本。

（English document is coming soon...）

## 预览

* [我的博客]
* [主题截图1](http://raytaylorlin-blog.qiniudn.com/%E4%B8%BB%E9%A2%98%E6%88%AA%E5%9B%BE1.jpg)
* [主题截图2](http://raytaylorlin-blog.qiniudn.com/%E4%B8%BB%E9%A2%98%E6%88%AA%E5%9B%BE2.jpg)
* [主题截图3](http://raytaylorlin-blog.qiniudn.com/%E4%B8%BB%E9%A2%98%E6%88%AA%E5%9B%BE3.jpg)
* [主题截图4](http://raytaylorlin-blog.qiniudn.com/%E4%B8%BB%E9%A2%98%E6%88%AA%E5%9B%BE4.jpg)

## 安装

```
cd yourblog
git clone https://github.com/raytaylorlin/hexo-theme-raytaylorism.git themes/raytaylorism
```

请不定期`git pull`一下主题以便获得最新的功能。

## 启用（重要）

1. 修改 `_config.yml` 中的`theme`一项的值为`raytaylorism`
2. 由于本主题使用了[Data Files]数据文件，所以**请复制`yourblog/themes/raytaylorism/_data`文件夹到`yourblog/source`目录下**，否则在启动server时会报错
3. 在你的`yourblog/_config.yml`配置文件的`#pagination`的位置添加下面配置（禁用归档、标签、目录页面的分页功能）

```
archive_generator:
  per_page: 0
tag_generator:
  per_page: 0
category_generator:
  per_page: 0
```

## 配置指南（重要）

* **主题颜色配置**：如果对主题的配色不满意，可以自行在`yourblog/themes/raytaylorism/_config.yml`中的`color`一项进行配置。其中各部件的颜色字符串命名遵循[Google Material Design色板]规范。
* **外部链接**：在`yourblog/source/_data/link.json`数据文件中进行配置
    * 社交平台：对应`social`项，预设有`weibo`和`github`两种，如果需要其他社交平台可自行追加，但要注意**key值必须与[Font Awesome图标]相对应，否则可能无法正常显示**。
    * 友情链接：对应`extern`项，其中key值为链接文字，value值为外链URL
* **首页幻灯片**：在`yourblog/source/_data/slider.json`数据文件中进行配置。可以配置背景图、标题、副标题、对齐方式。如果不需要幻灯片，直接把`slider.json`删除即可。
* **代码语法高亮**：语法高亮的主题默认由CSS文件`yourblog/themes/raytaylorism/source/css/lib/prettify-tomorrow-night-eighties.css`。如果需要替换，可以到[Prettify Theme]选择你喜欢的主题，下载主题的CSS文件并存放到相同的目录下，并将`yourblog/themes/raytaylorism/_config.yml`中的`google_code_prettify_theme`一项改为对应的文件名。
* **评论**：评论插件默认使用[多说]，需要自行配置`yourblog/themes/raytaylorism/_config.yml`中的`duoshuo_shortname`为你自己站点的shortname

## 使用的插件

* 样式框架：[Materialize]
* 代码语法高亮：[Google-code-prettify]
* 流量分析：[Google Analytics]
* 第三方社会化评论：[多说]

## 更新日志

* 1.3.0(2014-10-22) 新增文章中目录导航
* 1.2.9(2014-10-22) 修复主题在hexo 2.0+版本上运行报错的问题
* 1.2.8(2014-6-20) 添加MathJax插件
* 1.2.7(2014-5-4) 将读书栏目的书本封面固定宽高并按比例压缩，将详细展开标签置于封面右侧
* 1.2.6(2014-1-10) 添加分类目录菜单
* 1.2.5(2014-1-8) 修复升级hexo版本到2.3.0后，归档的标题没有显示的问题
* 1.2.4(2014-1-7) 修复Furatto升级版本后侧滑栏样式的问题
* 1.2.3(2014-1-4) 修复“加载更多”无法滚动的问题
* 1.2.2(2014-1-3) 重新调整全局的字体大小
* 1.2.1(2013-12-16) 修复升级hexo版本到2.3.0后，正文中代码排版的问题
* 1.2.0(2013-12-12) 修复当在hexo配置中new_feature_guide字段不存在时，生成会报错的问题
* 1.1.9(2013-11-1) 新增读书栏目
* 1.1.8(2013-10-24) 修复Furatto升级版本后各种样式的问题
* 1.1.7(2013-10-21) 修复Furatto升级版本后网格布局的显示错误
* 1.1.6(2013-10-18) 将Furatto升级到V2.0版本
* 1.1.5(2013-10-8) 修复在其他页面点击header的博客名没有回到首页的bug
* 1.1.4(2013-10-7) 新增about.ejs模板
* 1.1.3(2013-10-6) 修改新功能导航的DOM识别方式为查询字符串，给navbar的各项添加id
* 1.1.2(2013-10-3) 修复google_analytics.ejs中没有引用博客配置的错误
* 1.1.1(2013-9-20) 修复Google Analytics无效的bug
* 1.1.0(2013-9-20) 把新功能导航的特征值分离到博客的配置中
* 1.0.9(2013-9-19) 修复IE新功能导航阴影的显示问题
* 1.0.8(2013-9-19) 修复“你当前所在的位置”为空的bug
* 1.0.7(2013-9-18) 修复“加载更多”动画效果滚动不到位的问题
* 1.0.6(2013-9-15) 新增新功能导航效果
* 1.0.5(2013-9-5) 调整基础布局，新增首页加载更多按钮
* 1.0.4(2013-9-2) 针对手机进行响应式设计，重新定义所有版面的字体大小
* 1.0.3(2013-9-1) 新增响应式设计的侧滑菜单
* 1.0.2(2013-8-31) 添加了About页面并使用自定义模板
* 1.0.1(2013-8-26) 使页面主内容在高度不够的时候可以自适应屏幕，让页脚沉底

[Hexo]: http://hexo.io/
[我的博客]: http://raytaylorlin.com/
[Google Material Design色板]: https://www.google.com/design/spec/style/color.html#color-color-palette
[Font Awesome图标]: https://fortawesome.github.io/Font-Awesome/icons/
[Prettify Theme]: http://jmblog.github.io/color-themes-for-google-code-prettify/
[Materialize]: http://materializecss.com/
[Google-code-prettify]: https://code.google.com/p/google-code-prettify/
[Google Analytics]: http://www.google.com/analytics/
[Furatto]: http://icalialabs.github.io/furatto/
[Font Awesome]: http://fortawesome.github.io/Font-Awesome/
[多说]: http://duoshuo.com/
