FROM alpine:3.20
RUN apk add --no-cache tzdata ca-certificates
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime
WORKDIR /app
COPY Xiaoqing-blog-api/dist/Xiaoqing-blog-api /app/Xiaoqing-blog-api
RUN chmod 0755 /app/Xiaoqing-blog-api
EXPOSE 8080
USER nobody
ENTRYPOINT ["/app/Xiaoqing-blog-api"]
