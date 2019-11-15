# Add New Project
随着时间的推进以及项目的发展，目前此项目的目录结构不能满足日益增长的需求，所以会出现添加新文件/文件夹（项目）的情况，这里就把具体流程列举出来。  

## 1. 查看 Github 的提交
查看 GitHub 的提交（当前所在分支（branch）），保证自己当前所在分支为最新。  
如下图：
![分支查看](https://raw.githubusercontent.com/FrankWang1991/images/master/Screenshot 2019-11-15 at 16.45.22.png)

## 2. 创建文件/文件夹（项目）
最经常使用的功能是新增文件或者替换文件，但是也会遇到重新整理静态文件为文件夹或者新建文件夹，抑或是新建项目的需求，我们分别来看  
### 2.1 更新文件/新建文件
只需要在相应的文件目录下，使用 finder 或者其他查看工具，找到要替换的文件或者新建的文件的文件夹地址，创建文件/替换文件即可。
### 2.2 新建文件夹
新建文件夹的话和新建文件的方式相同，但是某些 git ui 工具（GitKraken/GithubDesktop）可能不能识别新增的空文件夹，这是可以在文件夹中创建任意文件。
### 2.3 创建项目
创建项目与创建文件夹完全相同，重要的是多了一步简单代码的指向。具体来说就是：  
这是目前的项目结构：  
![项目结构](https://raw.githubusercontent.com/FrankWang1991/images/master/4YGbMz.png)
我们新建一个项目（文件夹），名称为 `testFolder` ,里面包含一个 `index.html` 文件，为此项目的入口文件。
![新建项目文件目录](https://raw.githubusercontent.com/FrankWang1991/images/master/WV84qv.png)
这一步的最后一步就是修改最外层 `index.html` (目录为 `pharbers-design/index.html`)
我们主要修改的是 `line 21 - line 80` 这一区块的内容，我们页面展示一行四个项目的话，如果需要新建项目，可以将 `<section ...>...</section>` 之间的内容完全赋值到此 `section` 的下部，包含内容。如下所示： 

``` html
        <section class="container mb-2">
            <div class="card" style="width: 16rem;">
                <img src="./public/pharbers_logo_1.jpeg" class="card-img-top" alt="components">
                <div class="card-body">
                    <h5 class="card-title">Components Design</h5>
                    <p class="card-text">主要展示 pharbers company 的内部组件设计等，包含基础的颜色/字体/大小等，同时也有数据展示如表格等的组件。适用于 pharbers 项目.
                    </p>
                    <!-- <a href="#" class="btn btn-primary">查看</a> -->
                    <div class="btn-group">
                        <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown"
                            aria-haspopup="true" aria-expanded="false">
                            查看
                        </button>
                        <div class="dropdown-menu">
                            <a class="dropdown-item" href="./bp Design System/bpDS_General/index.html">General</a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item"
                                href="./bp Design System/bpDS_Navigiation/index.html">Navigiation</a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item"
                                href="./bp Design System/bpDS_Foundations/index.html">Foundations</a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item" href="./bp Design System/bpDS_Feedback/index.html">Feedback</a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item" href="./bp Design System/bpDS_DataEntry/index.html">DataEntry</a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item"
                                href="./bp Design System/bpDS_DataDisplay/index.html">DataDisplay</a>
                            <div class="dropdown-divider"></div>
                            <a class="dropdown-item"
                                href="./bp Design System/bpDS_Design Guideline/index.html">Guideline</a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="card" style="width: 16rem;">
                <img src="./public/img_login_ill.png" class="card-img-top" alt="TMIST">
                <div class="card-body">
                    <h5 class="card-title">NEW TMIST Design</h5>
                    <p class="card-text">Some description for TMIST design.</p>
                    <a href="./New Tmist UI/index.html" class="btn btn-primary">查看</a>
                </div>
            </div>
            <div class="card" style="width: 16rem;">
                <img src="./public/img_case-ucb.jpg" class="card-img-top" alt="ucb">
                <div class="card-body">
                    <h5 class="card-title">UCB Design</h5>
                    <p class="card-text">Some description for UCB design.</p>
                    <a href="./Tmist UCB UI/index.html" class="btn btn-primary">查看</a>
                </div>
            </div>
            <div class="card" style="width: 16rem;">
                <img src="./public/img_login.png" class="card-img-top" alt="ucb">
                <div class="card-body">
                    <h5 class="card-title">CHC Design</h5>
                    <p class="card-text">文件上传下载项目.</p>
                    <a href="./General UI/index.html" class="btn btn-primary">查看</a>
                </div>
            </div>
        </section>
        <section class="container mb-2">
            <div class="card" style="width: 16rem;">
                <img src="./public/pharbers_logo_1.jpeg" class="card-img-top" alt="components">
                <div class="card-body">
                    <h5 class="card-title">TestFolder</h5>
                    <p class="card-text">test folder description</p>
                    <div class="btn-group">
                        <button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown"
                            aria-haspopup="true" aria-expanded="false">
                            查看
                        </button>
                        <div class="dropdown-menu">
                            <a class="dropdown-item" href="./testFolder/index.html">test main</a>
                            <div class="dropdown-divider"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
```
主要修改的内容为 `section` 内部 `div` 的数量（为项目数量），以及此 `div` 内部 `img 中 src ` 以及 `h5` `p` 以及 
``` html 
<div class="dropdown-menu">
    <a class="dropdown-item" href="./testFolder/index.html">test main</a>
    <div class="dropdown-divider"></div>
</div>
```
效果：  
![result](https://raw.githubusercontent.com/FrankWang1991/images/master/QIL6X4.png)