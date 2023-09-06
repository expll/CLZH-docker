FROM golang:bullseye

# 设置GOPROXY环境变量。这里使用了公开的Go代理服务 goproxy.io。
ENV GOPROXY=https://goproxy.cn,direct

# 如果你想为某些私有模块或特定模块跳过代理，你可以设置GONOPROXY。
# ENV GONOPROXY=example.com,another.example.com

WORKDIR /clzh-go

COPY . .

RUN go mod init clzh-go
RUN go mod tidy
RUN go build -o main .

CMD ["./main"]
