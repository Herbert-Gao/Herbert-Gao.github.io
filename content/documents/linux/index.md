---
title: Linux
summary: Familiar with multiple linux distributions, Ubuntu, Debian, Kali, Deepin ...
date: 2023-10-1
type: docs
math: false
tags:
  - Shell, Bash, Zsh
image:
  caption: 'Kali linux feature with network security tools.'
---

I accessed to linux when I was still a Bachelor student.
I have tried to use Linux for my work and personal experiments, like CARLA, SUMO and ROS Ubuntu. 
Moreover, linux system on Arm based devices and x86 based devices are expericed during my working experience.
To explore more on Linux, I once installed Termux and AidLux (both are apps for emulating Linux) and code on the phone, trying to explore the Wi-Fi with python or compiling Latex in 2020.


**Embed videos, podcasts, code, LaTeX math, and even test students!**

On this page, you'll find some examples of the types of technical content that can be rendered with Hugo Blox.

## Video

Teach your course by sharing videos with your students. Choose from one of the following approaches:

{{< youtube D2vj0WcvH5c >}}

**Youtube**:

    {{</* youtube w7Ft2ymGmfc */>}}

**Bilibili**:

    {{</* bilibili id="BV1WV4y1r7DF" */>}}

**Video file**

Videos may be added to a page by either placing them in your `assets/media/` media library or in your [page's folder](https://gohugo.io/content-management/page-bundles/), and then embedding them with the _video_ shortcode:

    {{</* video src="my_video.mp4" controls="yes" */>}}

## Podcast

You can add a podcast or music to a page by placing the MP3 file in the page's folder or the media library folder and then embedding the audio on your page with the _audio_ shortcode:

    {{</* audio src="ambient-piano.mp3" */>}}

Try it out:

{{< audio src="ambient-piano.mp3" >}}

## Test students

Provide a simple yet fun self-assessment by revealing the solutions to challenges with the `spoiler` shortcode:

```markdown
{{</* spoiler text="👉 Click to view the solution" */>}}
You found me!
{{</* /spoiler */>}}
```

renders as

{{< spoiler text="👉 Click to view the solution" >}} You found me 🎉 {{< /spoiler >}}

## Math

Hugo Blox Builder supports a Markdown extension for $\LaTeX$ math. You can enable this feature by toggling the `math` option in your `config/_default/params.yaml` file.

To render _inline_ or _block_ math, wrap your LaTeX math with `{{</* math */>}}$...${{</* /math */>}}` or `{{</* math */>}}$$...$${{</* /math */>}}`, respectively.

{{% callout note %}}
We wrap the LaTeX math in the Hugo Blox _math_ shortcode to prevent Hugo rendering our math as Markdown.
{{% /callout %}}

Example **math block**:

```latex
{{</* math */>}}
$$
\gamma_{n} = \frac{ \left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T \left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}
$$
{{</* /math */>}}
```

renders as

{{< math >}}
$$\gamma_{n} = \frac{ \left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T \left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}$$
{{< /math >}}

Example **inline math** `{{</* math */>}}$\nabla F(\mathbf{x}_{n})${{</* /math */>}}` renders as {{< math >}}$\nabla F(\mathbf{x}_{n})${{< /math >}}.

Example **multi-line math** using the math linebreak (`\\`):

```latex
{{</* math */>}}
$$f(k;p_{0}^{*}) = \begin{cases}p_{0}^{*} & \text{if }k=1, \\
1-p_{0}^{*} & \text{if }k=0.\end{cases}$$
{{</* /math */>}}
```

renders as

{{< math >}}

$$
f(k;p_{0}^{*}) = \begin{cases}p_{0}^{*} & \text{if }k=1, \\
1-p_{0}^{*} & \text{if }k=0.\end{cases}
$$

{{< /math >}}

## Code

Hugo Blox Builder utilises Hugo's Markdown extension for highlighting code syntax. The code theme can be selected in the `config/_default/params.yaml` file.


    ```python
    import pandas as pd
    data = pd.read_csv("data.csv")
    data.head()
    ```

renders as

```python
import pandas as pd
data = pd.read_csv("data.csv")
data.head()
```

## Inline Images

```go
{{</* icon name="python" */>}} Python
```

renders as

{{< icon name="python" >}} Python

## Did you find this page helpful? Consider sharing it 🙌
Docker环境使用指南
Docker 环境运行在服务器上，是服务器上的一个虚拟机，在这个虚拟机内我们有高级权限，可以任意打造自己想做的事项，现在组内已经搭建好的docker环境有Ubuntu和mysql两个，本地overleaf暂无使用需求，因此尚未开启。
Docker环境使用分为两个步骤，一个是本地转发窗口，一个是利用软件连接。下面首先介绍下如何利用连接到组内公用的Ubuntu系统，及如何利用各个软件使用各个服务。其总的示意图如下：
 
步骤一：本地转发端口
利用ssh的内网穿透，实现本地转发端口，操控服务器上的虚拟机。不论是Mac、Linux 或是 Windows，打开命令行，执行下面语句 
 
步骤二：利用软件连接
这部分使用不同的软件连接到不同的服务，要使用Ubuntu系统，需要用到VNC软件，它是一种类似于Xshell远程的图形化界面，之后，在Ubuntu系统中使用matlab、python、C+代码开发或是carla仿真等工作；要使用MySQL服务，需要用到Navicat SQL软件，或其余你用的顺手的编辑器（VScode安装完SQL插件也可以）；要使用Overleaf服务，只需有个浏览器即可。
连接Ubuntu系统
公用Ubuntu系统地址为172.17.0.3:5902
使用VNC viewer 连接到Ubuntu系统
1.	安装VNC viewer按照以下教程
VNC Viewer安装教程（保姆级安装）_vncviewer-CSDN博客
安装比较简单，是个免费的软件，可直接官网安装，不激活也没关系。
2.	新建连接
选择File-New Connection
 
VNC server 填入本机的‘本地ip:端口号’，然后ok，双击新建的进行连接。
这里本地ip指的不是公网ip，而是电脑自己局域网的ip，如果不知道可以命令行ifconfig查看，win、linux默认是127.0.0.1，mac不知道。如果实在找不到ip，可以先尝试输入'localhost:端口号’；若还是不行，可以在上第一步端口转发时，就制定转发ip： ssh -fNL 127.0.0.1:5000:172.17.0.x:xxxx -p xxx ，仅多了指定转发到的ip号，其余不变。
如果如果连接成功，则会看到如下界面：
 
选择continue，提示输入密码
 
勾选记住密码，连接密码为 123123000，即可进入
 
不同于以往用的Ubuntu界面使用的红色的（Gnome），这个图形化界面是叫Xfce，是一个轻量级的，不占用太多计算资源。接下来就是使用Ubuntu内的服务。
服务器Carla环境的使用
Carla是基于Unity 虚拟游戏引擎 开发的仿真环境，已经部署到Ubuntu环境中，以下为使用教程。
进入carla文件夹，启动carla服务器端
 
carla采用的是服务器，加客户端的控制方式。但是渲染后传输数据量巨大，直接通过网络传输会有卡顿，所以建议直接在虚拟环境中运行程序。
Matlab使用
Ubuntu上的Matlab具有图形化界面，能够使用Simlink和工具包，使用的我的个人账户激活，若时间过期，请重新激活。以下为具体使用教程。
左上角application-开发工具development-matlab，打开matlab界面
自己代码保存/home 目录下自己姓名文件夹下

服务器MySQL环境的使用
SQL为管理大数据时所采用的框架，由甲骨文公司开发，被用在世界多数的数据存储中。
当我们从公共数据网站上下载大数据时，为了提高下载效率，网站存储的通常是单个数据文件，以GB为存储单位。直接打开会造成系统内存爆满，需要SQL来帮助我们管理并从中提取出有用的信息，存储为一个个的小文件，以方便我们之后使用数据。
关于SQL的具体使用细节请参考另一篇教程《MySQL的部署及使用教程》，这里仅对如何使用服务器上已经部署的MySQL环境使用进行介绍。
同样，已下仅看使用部分即可，运维部分请您熟悉linux操作、docker操作、进阶使用指南、mysql使用后，再对MySQL容器进行操作。

服务器overleaf环境的使用
由于世界上最大的文章编辑网站overleaf开始收费，需要一个新的环境进行合作编辑。幸运的是，overleaf项目是开源的，我们可以该项目部署到学院服务器上，相当于在学院服务器进行本地overleaf latex的编译操作，供我们组进行使用。
以下使用仅看使用部分即可，运维部分请您熟悉linux操作、docker操作、进阶使用指南后再对overleaf容器进行操作。
a.	本地转发容器窗口
b.	进入学院服务器overleaf

申请ieee账号后可以直接使用preium版本的overleaf，详情见：免费升级Overleaf Premium（IEEE Collabratec） - 知乎 (zhihu.com)