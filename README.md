# 使用说明：

```bash

1、添加代理 (临时有效)
export http_proxy=http://proxyAddress:port
export https_proxy=http://proxyAddress:port
export https_proxy=http://127.0.0.1:7890 && export http_proxy=http://127.0.0.1:7890
 export https_proxy=http://10.65.250.175:7890 && export http_proxy=http://10.65.250.175:7890
2、查看代理
env |grep -i proxy
3、清除代理
unset http_proxy
unset https_proxy
unset http_proxy https_proxy
4、运行
./clash -d .
./clash -f pathofconfig #配置文件路径
./clash -h 查看相关设置
./clash -d . -ext-ui ./clashUI/dashboard -ext-ctl '0.0.0.0:8092'  -f jinkela.yaml    #yaml文件为你的配置文件
后台运行
nohup ./clash -d . -ext-ui ./clashUI/dashboard -ext-ctl '0.0.0.0:8090'  -f haibin.yaml > info.log 2>&1 &

5、别名
alias clashon='export https_proxy=http://10.65.250.175:7890 && export http_proxy=http://10.65.250.175:7890'
alias clashoff='unset http_proxy https_proxy'
alias clashlist='env |grep -i proxy'
#永久生效，写入文件
vim /etc/bashrc
source /etc/bashrc

6、mihomo(新版clash终端)
https://github.com/MetaCubeX/mihomo
下载mihomo对应的deb包进行安装：
sudo apt install ./xxx.deb
运行：
mihomo -d .  -ext-ctl '0.0.0.0:8092'  -f xingjia.yml -ext-ui ./clashUI/mihomoui
webui为：metacubexd（yacd用不了）
    https://github.com/MetaCubeX/metacubexd
    external-controller: 0.0.0.0:9090（配置文件设置，可选）
```

# 配置参数，config.yaml文件
> 配置参考教程：   
https://wiki.metacubex.one/config/    
https://stash.wiki/configuration/example-config    
https://github.com/MetaCubeX/mihomo/blob/Meta/docs/config.yaml  





