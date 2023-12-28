# 使用官方的 Node.js 镜像
ARG NODE_IMAGE
FROM ${NODE_IMAGE}


# 设置工作目录
WORKDIR /www/openai-proxy

# 安装项目依赖
RUN npm install

RUN npm install -g pm2

# 暴露应用程序运行的端口（根据你的应用程序需要调整）
EXPOSE 9000

# 启动应用程序
CMD ["pm2", "start", "npm", "--", "start"]
# CMD ["npm", "start"]
