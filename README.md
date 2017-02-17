# repo 学习

主要是因为现在仓库越来越多，需要repo管理工具来做系统性的管理，其实主要还是在于编写[default.xml](default.xml)文件，这里的[default.xml](default.xml)也就是manifest.xml。

## 最终文件目录架构：
    .
    ├── git-repo                    # 获取的repo命令放这个文件夹里
    │   ├── ...
    │   ├── repo                    # 我们要用到的repo工具
    │   └── ...
    ├── manifest                    # 这个就是本仓库的内容了
    │   ├── .git
    │   ├── README.md
    │   └── default.xml             # 所谓的manifest.xml文件
    └── project                     # 测试上面manifest仓库编写的manifest.xml的目录
        ├── Android-Examples        # 获取的仓库
        ├── Linux-Examples          # 获取的仓库
        ├── manifest                # 获取的仓库
        ├── U-Boot                  # 获取的仓库
        ├── .repo                   # 测试过程中生成的.repo目录
        └── zh-cmn-Hans             # 获取的仓库

## 主要的操作步骤：
* 获取git-repo：
```
    $ git clone git://git.omapzoom.org/git-repo.git
```

* 初始化repo：
```
    $ ../git-repo/repo init -u git@github.com:ZoroZeng/manifest.git
```

* 同步仓库：
```
    $ ../git-repo/repo sync
```

* 创建分支：
```
    $ ../git-repo/repo start ZoroZeng
      error: project . not found
    $ ../gti-repo/repo branch
        (no branches)
    $ ../git-repo/repo start ZoroZeng --all
    $ ../gti-repo/repo branch
      * ZoroZeng                   | in all projects
```
