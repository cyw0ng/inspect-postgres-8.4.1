# PGDATA

- Get `PGDATA`, the backend:

```
root@56c0c353a3b9:/# env |grep PG
PG_MAJOR=8.4
PG_VERSION=8.4.22-1.pgdg70+1
PGDATA=/var/lib/postgresql/data

root@56c0c353a3b9:/var/lib/postgresql/data# ls -l
total 44
# 包含每个数据库目录，数据库以 OID 编号命名，OID == 1 的为 template1
drwx------ 5 postgres postgres    41 Aug  8 13:53 base
# 包含整个 cluster 的全局表，如 pg_database
drwx------ 2 postgres postgres  4096 Aug  8 13:53 global
# 事务提交状态
drwx------ 2 postgres postgres    18 Aug  8 13:53 pg_clog
# Host based ACL
-rw------- 1 postgres postgres  3680 Aug  8 13:53 pg_hba.conf
# 用户 UID 映射
-rw------- 1 postgres postgres  1631 Aug  8 13:53 pg_ident.conf
# 多重事务，用于共享的行锁
drwx------ 4 postgres postgres    36 Aug  8 13:53 pg_multixact
# 统计子系统的临时目录
drwx------ 2 postgres postgres    25 Aug  8 14:31 pg_stat_tmp
# 事务状态数据
drwx------ 2 postgres postgres    18 Aug  8 13:53 pg_subtrans
# 指向表空间的符号链接
drwx------ 2 postgres postgres     6 Aug  8 13:53 pg_tblspc
# 两阶段提交，预留事务状态
drwx------ 2 postgres postgres     6 Aug  8 13:53 pg_twophase
# 主版本号
-rw------- 1 postgres postgres     4 Aug  8 13:53 PG_VERSION
# 包含 WAL 的子目录
drwx------ 3 postgres postgres    60 Aug  8 13:53 pg_xlog
# 主配置
-rw------- 1 postgres postgres 16895 Aug  8 13:53 postgresql.conf
# 记录上一次启动的命令行参数
-rw------- 1 postgres postgres    37 Aug  8 13:53 postmaster.opts
# 锁文件，记录当前的 postmaster 进程 PID 和共享内存段 ID，随服务关闭时删除
-rw------- 1 postgres postgres    47 Aug  8 13:53 postmaster.pid
```