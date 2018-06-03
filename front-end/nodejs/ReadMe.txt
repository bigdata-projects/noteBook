npm太慢， 淘宝npm镜像使用方法
1.临时使用
npm --registry https://registry.npm.taobao.org install express
1
2.持久使用
npm config set registry https://registry.npm.taobao.org
1
配置后可通过下面方式来验证是否成功 
npm config get registry