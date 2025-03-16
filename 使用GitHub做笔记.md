# 使用GitHub做笔记

### **1. 创建 GitHub 仓库**

- 登录 [GitHub](https://github.com)。
- 点击右上角的 `+` → `New repository`。
- 取个合适的名字，比如 `algorithm-notes`，然后选择 `Public`（公开）或 `Private`（私有）。
- 勾选 `Add a README file`，方便写介绍。

注意：要使用图床上次图片必须选择 公开！！！

### **2. 组织你的算法笔记**

- 你可以按 数据结构/算法分类 组织，比如：

  ```
  bash复制编辑algorithm-notes/
  ├── README.md  # 介绍你的笔记
  ├── Sorting/   # 排序算法
  │   ├── quick_sort.md
  │   ├── merge_sort.md
  ├── Graph/     # 图论
  │   ├── bfs.md
  │   ├── dfs.md
  ├── LeetCode/  # 具体题目
  │   ├── 1_two_sum.md
  │   ├── 2_add_two_numbers.md
  ├── Code/      # 存放代码
  │   ├── quick_sort.java
  │   ├── bfs.java
  ```

### **3. 使用 Markdown 写笔记**

# 快速排序 (Quick Sort)

## **1. 思路**
快速排序使用**分治**思想，将数组分为左右两部分，然后递归排序。

## **2. 代码**
```java
public void quickSort(int[] arr, int left, int right) {
    if (left >= right) return;
    int pivot = partition(arr, left, right);
    quickSort(arr, left, pivot - 1);
    quickSort(arr, pivot + 1, right);
}
```

### **3. 提交到 GitHub**
本地创建仓库：
```bash
git init
git remote add origin https://github.com/你的用户名/algorithm-notes.git
git pull origin main
```

然后提交你的笔记：

```
bash复制编辑git add .
git commit -m "添加快速排序笔记"
git push origin main
```

### **5. 配合 LeetCode/GitHub Actions**

- 你可以每天 **记录 LeetCode 题解**，比如 `LeetCode/1_two_sum.md` 这样归档。
- 也可以用 GitHub Actions **自动同步代码**，比如定期拉取 LeetCode 题解。