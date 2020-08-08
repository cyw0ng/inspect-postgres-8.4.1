# initdb

- 初始数据库创建过程，通过 bootstrap 模式创建 cluster 并调用后端接口 postgres.bki 文件创建模板数据库

## postgres.bki

- 调用 genbki.sh 将所有 catalog 下的 header 定义创建为统一的 bki 文件
    - CATALOG 宏，统一模式定义表结构和描述
    - DATA/DESR 宏定义 insert 操作，用于填充模版数据
