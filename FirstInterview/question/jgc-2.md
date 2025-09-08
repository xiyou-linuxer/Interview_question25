## 10.拼接 排序 去重
本题要求你编写以下函数，要求不能改动 *main* 函数里的代码。
| 函数名       | 功能描述                                   |
| :----------- | :----------------------------------------- |
| your_concat  | 对 arr1 和 arr2 两个数组中的元素进行拼接，将结果放入 *result* 结构体中。 |
| your_sort    | 对放入 *result* 结构体中的元素进行排序        |
| your_dedup   | 对 *result* 结构体中的有序元素进行去重        |
```c
void print_result(result result) {
  for (int i = 0; i < result.len; i++) {
    printf("%d ", result.arr[i]);
  }
  printf("\n");
}

int main() {
  int arr1[] = {6, 1, 2, 1, 9, 1, 3, 2, 6, 2};
  int arr2[] = {4, 2, 2, 1, 6, 2};
  int len1 = sizeof(arr1) / sizeof(arr1[0]);
  int len2 = sizeof(arr2) / sizeof(arr2[0]);

  result result;
  your_concat(arr1,len1,arr2,len2,result);
  print_result(result);
  your_sort(result);
  print_result(result);
  your_dedup(result);
  print_result(result);
  free(result.arr);
  return 0;
}
```
---
| **出题人** | **井光成**                 |
| ------- | ---------------------- |
| 知识点1    | 动态内存分配与结构体设计           |
| 知识点2    | 参数传递 |
| 知识点3    | 排序算法            |
| 知识点4    | 去重算法与边界处理              |
| 知识点5    | 时间复杂度与空间复杂度分析          |
---
Q1：说出你熟悉的排序算法，并简述一下其中思想
Q2：时间复杂度，空间复杂度，分析排序算法的时间复杂度
Q3：去重算法，如何想的