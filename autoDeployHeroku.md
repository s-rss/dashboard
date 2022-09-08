# Heroku 自动部署 GitHub 代码

1、打开 heroku 应用列表，选择一个 app 进入

![image-20220908223051428](https://cdn.jsdelivr.net/gh/MrSeaWave/figure-bed-profile@main/uPic/2022/aNB98P_image-20220908223051428.png)

2、点击 deploy 选项卡，在 Deployment method 栏选择 GitHub

![image-20220908223156778](https://cdn.jsdelivr.net/gh/MrSeaWave/figure-bed-profile@main/uPic/2022/Mq2oTv_image-20220908223156778.png)

3、在 Connect to GitHub 栏搜索 GitHub 上的项目，在需要部署的项目右侧点击 connect

![image-20220908223451901](https://cdn.jsdelivr.net/gh/MrSeaWave/figure-bed-profile@main/uPic/2022/e8EbtW_image-20220908223451901.png)

4、在 Automatic deploys 栏 点击 Enable Automatic Deploys

![image-20220908223601855](https://cdn.jsdelivr.net/gh/MrSeaWave/figure-bed-profile@main/uPic/2022/SvdoJD_image-20220908223601855.png)


然后就可以在每一次 git push 到 GitHub 后就会自动部署到 Heroku 了

> Tips: 
> 
> 部署之前我们需要创建一个类似启动脚本的文件 Procfile
> ```
> // Profile 
> web: node lib/index.js
> ```
> 这个文件告诉 Heroku需要创建一个web 容器, 同时执行 node lib/index.js 来启动程序，更多的详细信息在这里 [Process Types and the Procfile](https://devcenter.heroku.com/articles/procfile)


## 参考链接

- [在 Heroku 上开发、部署Node程序的快速指南](https://segmentfault.com/a/1190000013987807)
