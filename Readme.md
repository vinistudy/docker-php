### 安装

```
git clone .
cp .env.example .env
cp compose.yaml.example compose.yaml
```
可以自己修改 `.env` 和 `.compose.yaml` 的配置。

### 使用

```
# -p 项目名字
# -f compose 文件
docker-compose -p docker-test -f ./compose.yaml up -d

# 停止
docker-compose down

# 启动
docker-compose start
```

### 开发本地 nginx 域名映射

修改 host，加入域名配置。

```
# eg

192.168.0.1 docker.zeipan.com
```