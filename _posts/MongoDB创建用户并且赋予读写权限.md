---
title: MongoDB创建用户并且赋予读写权限
cid: 4
created: 1741325738
modified: 1741325738
categories:
  - 技术笔记
  - 数据库
---

```bash
db.createUser({
  user: "myUser",
  pwd: "myPassword",
  roles: [
    { role: "readWrite", db: "mydatabase" },
    { role: "read", db: "anotherdatabase" }  // 只有读权限
  ]
});
```
