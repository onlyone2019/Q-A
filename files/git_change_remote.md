# 改变本地git仓库关联的远程仓库

错误信息：`fatal: remote origin already exists. `

```C++
git remote rm origin  //删除与远程的关联

git remote add origin git@github.com:(github名)/(git项目名).git //重新关联
```