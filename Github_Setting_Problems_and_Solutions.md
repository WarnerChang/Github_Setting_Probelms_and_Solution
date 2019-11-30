# Github常见问题及解决方案 #

## 问题一：fatal: not in a git directory ##

1.问题场景：用户之前一直使用web端创建仓库及upload files，当某一天突然发现github限制了上传文件的大小，导致上传失败；于是在项目所在文件夹(其实用户并未创建所谓的项目文件件)启用git客户端，然后输入命令“git config http.postBuffer 524288000”，接着使用“git config -l”命令查看git配置；然而却报错“fatal: not in a git directory”

2.解决方案1：

    ① 创建项目文件夹

    ② 在项目文件夹下启用git客户端

    ③ 键入命令“git add .”，作用为提交文件(当然可以先修改上传文件大小限制)

    ④ 键入命令“git commit -m "..." ”，省略号中可以为任意字符

    ⑤ 键入命令“git push origin master”命令将文件推送给服务器

解决方案2：

    ① 在待上传文件所在目录启用git终端

    ② 键入“git init”命令

    ③ 键入“git config http.postBuffer 524288000”命令

    ④ 键入“git config -l”命令

    ⑤ 键入“git add+文件名”命令

    ⑥ 键入“git push -f origin master”命令，注意在web端的GitHub设置默认的master，且会存在文件覆盖现象

***

注意：

git终端中，不可以采用“Ctrl+C”及“Ctrl+V”组合键，使用鼠标选中待复制内容即可实现复制；“粘贴”需要单击右键，选中paste

***


