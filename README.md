# 本地启动步骤
1. 创建config.yaml文件，配置账户和密码
2. NodeJS版本为18.0.0以上
3. 执行`npm run dev`命令

# Docker部署

```shell
docker build -t wechat-chatgpt:v1.0 .

docker run -d --name wechat-chatgpt -v $(pwd)/config.yaml:/app/config.yaml holegots/wechat-chatgpt:latest

# 通过二维码登录
docker logs -f wechat-chatgpt
```