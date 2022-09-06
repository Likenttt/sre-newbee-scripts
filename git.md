## Git

### 奇技淫巧

#### 删除已经提交的文件

```bash
#bin下的文件是构建产生的，根本不需要提交到远程，所以直接删除并重写历史。
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch bin/*' --prune-empty --tag-name-filter cat -- --all
git push origin dev:dev --tags --force
```
