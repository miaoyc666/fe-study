nodejs
=


### base
#### nodejs install
```bash
# 官方文档：https://github.com/nodesource/distributions
# 查看最新版本安装方式：https://rpm.nodesource.com/
# 示例如下
# yum
curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
yum install -y nodejs

# apt
curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh
sudo -E bash nodesource_setup.sh
sudo apt install -y nodejs

# mac安装node
brew install node
```

#### pnpm install
```bash
# npm是随node一起安装的包管理器
# pnpm是用于解决npm的node_modules中包重复安装的问题，而推出的npm替代品
npm install -g pnpm
# 卸载
npm uninstall -g pnpm
```

#### set npm source 
```
npm config set registry https://registry.npmjs.org/
```

