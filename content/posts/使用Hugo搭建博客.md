# 使用Hugo搭建博客

我的搭建过程记录在Notion中，与原博客自动同步，因格式不易调整，只粘过来部分内容

完整博客请见：[使用Hugo搭建博客 (easyone.top)](https://blog.easyone.top/OSSDT-hugo-deploy)

# 部署过程中遇到的问题
- 问题1：主题部署后页面无改变
  
    ![找不到名叫”paper”的主题，因为我直接下载，解压后名为”hugo-paper-main”](https://raw.githubusercontent.com/Sunny2567/PicBed/main/Capture8.PNG)
    
    找不到名叫”paper”的主题，因为我直接下载，解压后名为”hugo-paper-main”
    
    应保证配置文件`hugo.toml`中theme属性值和站点目录themes下的主题名称一致
    
    ![修改一致后问题解决](https://raw.githubusercontent.com/Sunny2567/PicBed/main/Capture9.PNG)
    
    修改一致后问题解决
    
- 问题2: Author identity unknown
  
    解决方案1: 先把GitHub Desktop登录了，会自动设置
    
    解决方案2: 按照提示信息设置 `user.name` 和 `user.email`
    
- 问题3: 上传后网页无法访问，提示404
  
    ![Capture14.PNG](https://raw.githubusercontent.com/Sunny2567/PicBed/main/Capture14.PNG)
    
    如果提示如图中所示，这里没有站点，一般是仍在审核的原因。
    
    ![CleanShot 2023-06-29 at 16.34.20@2x.png](https://raw.githubusercontent.com/Sunny2567/PicBed/main/Capture16.png)
    
    通过查看Actions中的提示信息，我们发现项目仍在等待审核。
    
    一般来讲，等5分钟如果还没过就不会过了，请检查前面提到的第一篇博客名字以及第一次Commit(提交)的名字是否包含myBlog，如不包含建议删除仓库，修改后重新上传。
    
    如果提示信息不是图中的，但提示404，一般是站点配置问题，请对照教程检查你是否完整地上传了要求的文件。文件夹选没选对。
    

![部署成功](https://raw.githubusercontent.com/Sunny2567/PicBed/main/Capture15.png)
部署成功

# 拓展：自动化部署

我阅读官方文档并使用GitHub Action 实现了自动化部署，请见完整博客。

使用Hugo搭建博客 (easyone.top)](https://blog.easyone.top/OSSDT-hugo-deploy)
