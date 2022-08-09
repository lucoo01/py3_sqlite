# py3_sqlite
Python3 连接sqlite数据库 增删改查简单封装

## 使用说明
```sql
-- 生成实例
db = SqliteDB()

-- 创建表格
sql = "CREATE TABLE asin (id INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL, asin VARCHAR, status VARCHAR, title VARCHAR, cover VARCHAR, stars double, lreviewdate VARCHAR, description VARCHAR, url VARCHAR, atime timestamp NULL DEFAULT NULL, mtime timestamp NULL DEFAULT NULL, price double, flag INTEGER DEFAULT 0, reviewcount INTEGER DEFAULT 0)"
res = db.createtb(sql=sql,table='asin')
print(res)

-- 插入
cs = db.insert(table="asin", asin=asin, title="标题", stars=4.3)
print(cs)

-- 删除
cs = db.delete(table="asin", where="id=6")
print(cs)

-- 更新
cs = db.update(table="asin", title="8888", stars=4.9, where="id=2")
print(cs)

-- 查询
cs = db.getAll(table="asin", where="1")
print(cs)

```

