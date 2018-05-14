## 安装zsh
``sudo apt-get install -y zsh``

## 安装 oh-my-zsh
``wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | sh``

## 设置zsh为默认shell
``chsh -s /bin/zsh root``

## 插件
+ wd：给指定目录映射一个全局的名字，以后方便直接跳转到这个目录，比如：我常去目录： **/opt/setups**，每次进入该目录下都需要``cd /opt/setups``,现在用 wd 给他映射一个快捷方式``cd /opt/setups ; wd add setups``,以后我在任何目录下只要运行``wd setups``就自动跑到 **/opt/setups** 目录下了
[插件官网](https://github.com/mfaerevaag/wd)
+ autojump
  + 插件下载：wget https://github.com/downloads/wting/autojump/autojump_v21.1.2.tar.gz
  + 解压：tar zxvf autojump_v21.1.2.tar.gz
  + 进入解压后目录并安装：cd autojump_v21.1.2/ ; ./install.sh
  + 编辑配置文件，添加上 autojump 的名字：vim /root/.zshrc
+ zsh-syntax-highlighting
  + 安装：``git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting``
  + 编辑：``vim ~/.zshrc``，找到这一行，后括号里面的后面添加：plugins=( 前面的一些插件名称 zsh-syntax-highlighting)
  + 刷新下配置：``source ~/.zshrc``

[配置参考链接](https://blog.csdn.net/u010138906/article/details/78778627)
