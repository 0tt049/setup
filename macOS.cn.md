# 电脑设置教程

以下的教程将会帮助你为接下来在[Le Wagon](http://www.lewagon.org) 全栈开发训练营中做好准备：

- 获取一个文本编辑器，这里将会是你日日夜夜花时间的地方
- 安装一个软件包管理器
- 装扮你的终端
- 配置git和GitHub
- 安装Ruby

## 远程工具

为了能让我们不在一起的时候也能很好的沟通，我们将会使用以下两个工具：

### Zoom

⚠️ 如果你已经安装了Zoom，请确保你Zoom的版本不低于**5.4**。否则，你将不能使用分组讨论室来和你的伙伴一起工作。

Zoom是一个视频会议工具。想要创建账户并安装这个应用，你需要到[https://zoom.us/download](https://zoom.us/download)这个网页，并在**Zoom会议客户端（Zoom Client for Meetings）**下方点击**下载（Download）**按钮。打开你刚下载好的文件。将出现一个进度条，然后Zoom便会开始。点击**Connection** 并创建一个账户，选择**Sign Up Free**选项：

![zoom-sign-up-free.png](images/zoom-sign-up-free.png)

当你连接成功后，你将会看到:

![zoom-welcome-screen.png](images/zoom-welcome-screen.png)

现在你可以关闭Zoom了。


## 检查你的电脑是否为Apple Silicon(Apple M1芯片)

如果你是在2020下半年买的电脑，它更有可能是Apple Silicon而不是Intel处理器。让我们来查看查看...

你可以从Applications > Utilities或者在[Spotlight](https://support.apple.com/en-gb/HT204014)里面搜索：

![](images/open-terminal.png)

复制粘贴以下的指令到终端里并按`Enter`来执行这段指令。

``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/lewagon/setup/master/utils/osx_list_processor_type.sh)"
```

☝️执行完这段代码之后将会表明你的电脑是否使用的是Apple Silicon。

如果你的电脑使用的是Apple Silicon，展开下面的段落并进行阅读。如果不是的话，请忽略它。

<details>
  <summary>👉&nbsp;&nbsp;Setup for Apple Silicon 👈</summary>

  &nbsp;



## Apple Silicon的相关设置

### 卸载Homebrew

我们需要卸载Homebrew以防本地已经安装了一个版本。

在终端中执行以下代码:

``` bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
```

如果brew如果没有被安装，你将会得到以下消息`brew: command not found!`

### 为Rosetta配置终端

打开访达Finder（或者在[Spotlight](https://support.apple.com/en-gb/HT204014)里搜索它)。

前往Applications > Utilities.

复制终端应用(选择它, 然后Cmd + C, Cmd + V)，并将它的复制重命名为Terminal Rosetta。

在Terminal Rosetta软件上按Cmd + I, 然后勾选”使用Rosetta打开（Open using Rosetta）“.

⚠️ 从此以后在训练营中，每当你需要打开终端的时候，你将需要打开**Terminal Rosetta**应用。

启动终端应用程序。将会跳出安装Rosetta窗口。点击安装。

</details>

## 一个有关在mac上跳出应用程序的小贴士

在mac上点击应用程序窗口左上方的小红叉**并不是真正的退出了它**，他只是关闭了一个活跃窗口。如果想要 _真正_ 的退出应用程序，你需要在应用活跃的时候按`Cmd + Q`，或者在你的菜单栏里前往`APP_NAME` -> 点击`Quit`

![quit.png](images/quit.png)

在这个设置教程中，你将会被要求**退出并重启**应用程序很多次，请确保你可以正确的退出重启 :pray:

## 命令行工具

从Applications > Utilities或者[Spotlight](https://support.apple.com/en-gb/HT204014)搜索，打开一个新的终端窗口。

复制粘贴以下指令到你的终端并按下`Enter`来执行指令。

```bash
xcode-select --install
```

如果你收到了以下消息，你可以直接就跳过这一步并前往下一步。

```
# command line tools are already installed, use "Software Update" to install updates
```

不然的话，他将会打开一个窗口询问你是否想要下载一些软件。同意并等待。如果失败了，在重新尝试一下`xcode-select --install`这个指令，有的时候Apple服务器会过载。

![](images/xcode-select-install.png)

当你下载的时候，你可以继续前往GitHub账户的设置，但是要在Homebrew章节前**停下来**。你将需要安装好的命令行工具来执行那一章节。

如果你收到了以下消息，你需要更新软件更新目录。

```
Xcode is not currently available from the Software Update server
```

如果遇到这种情况的话，你需要复制粘贴以下指令并按下Enter。

```bash
sudo softwareupdate --clear-catalog
```

这个执行结束之后，你可以尝试再一次安装（复制粘贴以下指令并按下Enter）。

```bash
xcode-select --install
```

然后你便可以继续接下来的教程啦。


## GitHub账户

你有注册好GitHub账户嘛？如果还没有，[现在注册](https://github.com/join)。

:point_right: **[上传一张照片](https://github.com/settings/profile)** 并在你的GitHub账户中设置你的名称。这一步很重要，因为我们将使用一个带有你头像的内部dashboard。请**现在**立即做这一步，然后再去继续下面的步骤。

![](images/github_upload_picture.png)

## Homebrew

在Mac上，你需要安装[Homebrew](http://brew.sh/)，一个包管理工具。我们将在安装一些软件的时候用到它。

想要安装，你需要打开终端并执行：

```bash
/bin/bash -c "$(curl -fsSL https://web-dev-challenge-lewagon-image.oss-cn-shanghai.aliyuncs.com/setup/install_hb.sh)"
```

这将会询问你的确认（按下`Enter`）并输入你的**macOS用户账户密码**（那个当你重启你Macbook时，用来[登入](https://support.apple.com/en-gb/HT202860) 的密码）。
:warning:当你在终端输入密码的时候，你将**看不到**任何视觉反馈（类似`*****`），这是**正常的**！直接输入密码并按下`Enter`来确认。

如果你已经有了Homebrew,终端会告诉你的。那么一切正常，你可以继续接下来的步骤。

接下来，让我们安装一些有用的软件：

```bash
brew update
```

如果你得到了`/usr/local must be writable`的报错，直接运行以下指令：

```bash
sudo chown -R $USER:admin /usr/local
brew update
```

无论是否有这行报错，继续执行下方的指令（你可以一次性直接复制/粘贴下方所有行）

```bash
brew upgrade git         || brew install git
brew upgrade gh          || brew install gh
brew upgrade wget        || brew install wget
brew upgrade imagemagick || brew install imagemagick
brew upgrade jq          || brew install jq
brew upgrade openssl     || brew install openssl
```

## Sublime Text 3 - 你的文本编辑器

一个文本编辑器是开发人员最重要的工具之一。前往[这个页面](http://www.sublimetext.com/3) 并下载OS X版本的**Sublime Text 3**。安装它（双击下载好的文件，拖动应用程序**放入到**`应用程序 Application`文件夹，**不要跳过这一步**）。如果你之前安装过Sublime Text 2，请先卸载它（把它拖动到垃圾桶）。

Sublime Text是免费且没时限的，但会在每十次储存之后跳出一个弹窗，提示你去购买license牌照。在这种情况发生的时候，你可以按`Esc`，但你也可以选择去购买Sublime Text如果你真的喜欢的话（当然还是有其他文本编辑器的选择的）。

再一次，确保Sublime Text安装好了，而不是在你下载的磁盘镜像里。为了确保所有步骤执行正确，当Sublime Text安装完成后，
卸载Finder左侧面板中的“ Sublime Text 3”磁盘。如果有什么出错的话，Finder会报错。这时可以询问一下老师。

## Oh-my-zsh - 美化你的终端

我们将使用一个叫做`zsh`的shell，取代默认的`bash`，并使用有用炫酷的[`oh-my-zsh`](https://ohmyz.sh/)插件：

```bash
sh -c "$(curl -fsSL https://web-dev-challenge-lewagon-image.oss-cn-shanghai.aliyuncs.com/setup/install_ohmyzsh.sh)"
```

注意，在这个脚本的最后，它会再次提示输入你macOS用户账户密码（记住！终端上不会在你输入密码的时候给你视觉反馈！）。你会类似以下的东西：

```bash
         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/                       ....is now installed!
````

现在退出终端（`⌘` + `Q`）并重启它。

你会看到以下内容：

![](images/on-my-zsh.png)

如果没有的话，**立马停下来**并寻求老师的帮助。

在Mac上，打开`Terminal > Preferences`并在`Profiles`中将“Pro”主题设置为默认。

![](images/terminal-pro.png)

**退出**并重启终端。它现在会有一个好看的黑色背景，对眼睛会更友好。

:bulb: 如果你想尝试其他主题的话，网上有许多可用的主题，比如[MaterialDark](https://github.com/lysyi3m/macos-terminal-themes#materialdark-download)。换主题的部分你可以在你其他设置都设置好后，回头继续做。请先继续Github的设置！

## Apple Silicon

<details>
  <summary>忘记你的电脑是否是使用Apple Silicon的了?</summary>

  &nbsp;

  复制粘贴下方的代码到终端中并按下`Enter`来执行指令。

  ``` bash
  /bin/bash -c "$(curl -fsSL https://web-dev-challenge-lewagon-image.oss-cn-shanghai.aliyuncs.com/setup/osx_list_processor_type.sh)"
  ```

  ☝️ 这个指令的输出可以显示你的电脑是否是使用Apple Silicon的。

</details>

如果你的电脑使用**Apple Silicon**，运行以下指令。如果不是，请忽略它。

``` bash
echo 'export RUBY_CONFIGURE_OPTS="--with-openssl-dir=$(brew --prefix openssl@1.1)"' >> ~/.zshrc
```

## GitHub

## GitHub CLI

## Dotfiles (Standard configuration)

### Sublime Text 自动配置

打开一个新的终端并输入：

```bash
cd ~/code
stt
```

它将会**在Sublime Text中打开当前文件夹**。这是我们如何使用它的方法。

**关闭Sublime Text**并重新打开它：

```bash
stt
```

**等待一分钟**，等所有额外的软件包都自动安装好（会自动打开一个带有文本的新的窗口，上面会包含每个你安装好的新包的文档）。如果想要跟踪软件包的安装进度，你可以前往`View > Show console`。

如果想要核查是否所有的插件都安装好了，你可以打开`命令面板 Command Palette`(在OSX上，按下`⌘` + `⇧` + `P`；在linux上，按下`Ctrl` + `⇧` + `P`)，输入`Packlist`然后按`Enter`，你应该会看到有一些软件包被安装了（像是[Emmet](http://emmet.io/)）。

当这些结束之后，你可以关闭Sublime Text。

### SSH 密钥

在一个终端窗口，启动这个命令：


```bash
sw_vers
```

<details>
  <summary>点击这里，如果你的OS版本（版本号）低于10.12</summary>

  为了避免每一次`git push`的时候，重新输入你的SSH密钥，你可以添加以下这些行到你的`~/.ssh/config`文件中：

  首先，打开`~/.ssh/config`文件：

  ```bash
  touch ~/.ssh/config  # Creates the file if it does not exist
  st ~/.ssh/config     # Opens the file in Sublime text
  ```

  然后，添加以下三行到这个文件中。**记得保存**。


  ```bash
  Host *
    AddKeysToAgent yes
    UseKeychain yes
  ```
</details>


## 安装Ruby (使用[rbenv](https://github.com/sstephenson/rbenv))

首先，我们需要先清理我们之前可能安装过的Ruby:

```bash
rvm implode && sudo rm -rf ~/.rvm
# 如果出现"zsh: command not found: rvm"报错, 继续后续的步骤. 这是指 `rvm` is not
# on your computer, that's what we want!

sudo rm -rf $HOME/.rbenv /usr/local/rbenv /opt/rbenv /usr/local/opt/rbenv
```

现在让我们来通过Homebrew来获取[`rbenv`](https://github.com/rbenv/rbenv)和[`ruby-build`](https://github.com/rbenv/ruby-build)，他们将会很有用。

```bash
brew uninstall --force rbenv ruby-build
```

然后退出**所有你打开着的终端窗口**（Cmd + Q)并重启新的一个。然后运行：

```bash
brew install rbenv
```

再一次，退出所有你的终端窗口并重启。

现在，你已经准备好了去安装最新Ruby版本并把它设置为默认版本。

运行下方这个指令，它会**花费一些时间（5-10分钟）**

```bash
rbenv install 2.6.6
```

当Ruby安装好后，运行下面这个指令来告诉系统使用2.6.6这个版本作为默认版本。

```bash
rbenv global 2.6.6
```

然后再次**重启**你的终端（关掉并重新打开它）。

```bash
ruby -v
```

你应该会看到`ruby 2.6.6p`。如果没有的话，询问一下老师。

## 安装一些gems

---

<details>
  <summary>点击这里，如果你在 :cn: <bold>中国</bold>的话</summary>


  &nbsp;

  :warning: 如果你在中国的话，你应该使用以下命令来安装gem。

```bash
# China only!
gem sources --remove https://rubygems.org/
gem sources -a https://gems.ruby-china.com/
gem sources -l
# *** CURRENT SOURCES ***
# https://gems.ruby-china.com/
# Ruby-china.com must be in the list now
```
</details>

---

无论你是不是在中国，请都运行下面的指令：

```bash
gem install rake bundler rspec rubocop rubocop-performance pry pry-byebug colored http
```

如果你遇到了以下的报错：

`
ERROR: While executing gem ... (TypeError)
incompatible marshal file format (can't be read)
format version 4.8 required; 60.33 given
`

运行以下的指令：

```bash
rm -rf ~/.gemrc
```

然后，重新运行安装gems的指令。

**永远不要**使用`sudo gem install`来安装一个gem！即使你偶然发现了一个网络上的答案（或者终端提示）叫你这么做。

## Node (使用[nvm](https://github.com/nvm-sh/nvm))

```bash
curl -o- https://web-dev-challenge-lewagon-image.oss-cn-shanghai.aliyuncs.com/setup/install_nvm.sh | zsh
```

重启你的终端并执行下方指令：

```bash
nvm -v
```

你应该会看到你的nvm的版本。如果没有的话，问一下你的老师。

现在，让我们来安装node：

```bash
nvm install 14.15.0
```

当这个指令执行结束之后，运行：

```bash
node -v
```

你应该会看到`v14.15.0`。如果没有的话，问一下你的老师。

## yarn

让我们一起来安装[`yarn`](https://classic.yarnpkg.com/en/docs/install):

```bash
npm install --global yarn
```

重启终端并运行：

```bash
yarn -v
```

你应该会看到你yarn的版本。如果没有的话，问一下你的老师。

## PostgreSQL

我们在之后将会用几周的时间，来学习SQL和数据库。你将会需要一个叫做PostgreSQL的东西，一个开源的可用于生产的强大数据库。让我们现在一起安装它。

```bash
brew install postgresql
brew services start postgresql
```

当你结束了上方的指令之后，让我们一起来核查一下它是否安装成功了：

```bash
psql -d postgres
```

如果你进入到了一个像下方这个，一个新的输入框的话，那么说明你的PostgreSQL已经安装好啦！

```bash
psql (12.5)
Type "help" for help.

postgres=#
```

如果想要退出它的话，输入`\q`然后按下`Enter`。


## 安全

你必须使用密码来保护你的电脑。如果你还没有设置过密码的话，请前往`>系统偏好设置>用户和组`并更改您的帐户密码。您还应该前往`>系统偏好设置>安全性>通用`。睡眠或屏幕保护程序启动的`5秒`后，您应该要求输入密码。

您也可以前往` > 系统偏好设置 > 任务控制`，然后单击左下角的`Hot Corners`按钮。选择右下角以启动屏幕保护程序。这样，当您离开办公桌时，可以通过将鼠标置于右下角来快速锁定屏幕。5秒钟后，您的Macbook将被锁定，并要求输入密码以恢复。

## 最后检查

让我们来看看你是否已经成功安装好了所有软件。

退出所有的终端，打开一个新的终端窗口并运行下方指令：

```bash
curl -Ls https://web-dev-challenge-lewagon-image.oss-cn-shanghai.aliyuncs.com/setup/check.rb > _.rb && ruby _.rb || rm _.rb
```

它应该会告诉你，你的工作台是否已经正确的设置好了 ：）如果没有的话，问一下你的老师。


## 校友
:warning: 如果你已经收到了一封来自Le Wagon邀请你去注册Kitt(我们的学习平台)的邮件并且你也注册完成了的话，你可以安全的跳过这一章节。如果你还没有注册完成的话，请跟随邮件里的教程，完成注册。

如果你不确定你要做什么，可以查看[这个链接](https://kitt.lewagon.com/)。如果你已经登录了的话，你可以跳过这个章节。如果你没有登录的话，你需要点击`Enter Kitt as a Student`。如果你可以成功的登录，你也可以安全的跳过这一步。不然的话，你可以询问一下老师你是否有收到过相关的邮件，或者直接跟着执行下面的教程。

前往[kitt.lewagon.com/onboarding](http://kitt.lewagon.com/onboarding)，注册成为Le Wagon的一名校友。选择你的batch，用gitHub账户登录并填写你的信息。

Your teacher will then validate that you are indeed part of the batch. You can ask him to do it as soon as you completed the registration form.

Once the teacher has approved your profile, go to your email inbox. You should have 2 emails:

- One from Slack, inviting you to the Le Wagon Alumni slack community (where you'll chat with your buddies and all the previous alumni). Click on **Join** and fill the information.
- One from GitHub, inviting you to `lewagon` team. **Accept it** otherwise you won't be able to access the lecture slides.


## Slack

## 键盘

### 键盘速度

### 全部键盘权限

### 黑客的macOS


































