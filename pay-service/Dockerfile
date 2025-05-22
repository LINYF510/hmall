# 基础镜像
FROM openjdk:11.0-jre-buster

# 设定时区
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# 拷贝jar包
COPY pay-service.jar /app.jar

# 声明容器运行时监听的端口（关键修改）
EXPOSE 8086

# 入口
ENTRYPOINT ["java", "-jar", "/app.jar"]
