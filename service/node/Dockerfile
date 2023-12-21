# 使用官方的 Node.js 镜像
FROM node:14

# 复制应用程序代码到工作目录
COPY ./node-dss /www

RUN if [ -d /www/node-dss ]; then \
      RUN git clone https://github.com/bengreenier/node-dss /www/node-dss \
    fi

# 设置工作目录
WORKDIR /www/node-dss

# 安装项目依赖
RUN npm install

RUN npm install -g pm2

# 暴露应用程序运行的端口（根据你的应用程序需要调整）
EXPOSE 3000

# 启动应用程序
CMD ["pm2", "start", "npm", "--", "start"]
# CMD ["npm", "start"]
