# Go语言CRUD实践 - 电影管理

## 概述

本项目是一个用于练习CRUD（创建、读取、更新、删除）操作的电影管理系统，使用 Go 语言和 Gorilla Mux 路由库实现。它提供了一个
RESTful API，允许用户通过 HTTP 请求管理电影信息。系统使用内存中的切片来临时存储数据，因此服务重启后数据将丢失。

## 功能

- **获取所有电影**: 列出系统中存储的所有电影。
- **获取单个电影**: 根据电影 ID 获取特定电影的详细信息。
- **创建新电影**: 添加一个新的电影到系统中。
- **更新电影信息**: 修改已存在的电影信息。
- **删除电影**: 根据电影 ID 从系统中删除一个电影。

## 技术栈

- **Go**: 用于后端服务的主要编程语言。
- **Gorilla Mux**: 用于处理 HTTP 请求的路由库。

## 安装和运行

确保你的系统已经安装了 Go。

1. 克隆仓库到本地:
   ```bash
   git clone [你的仓库地址]
   cd [仓库名称]
   ```
2. 运行服务:
   ```bash
   go run main.go
   ```

服务默认在 8000 端口启动。你可以通过访问 http://localhost:8000/movies 来测试是否运行成功。

## API 接口说明

- `GET /movies`: 获取所有电影的列表。
- `GET /movies/{id}`: 获取指定 ID 的电影详细信息。
- `POST /movies`: 创建一个新的电影记录。
- `PUT /movies/{id}`: 更新指定 ID 的电影记录。
- `DELETE /movies/{id}`: 删除指定 ID 的电影记录。
