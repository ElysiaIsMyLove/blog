#include <stdio.h>

int main() {
    printf("请输入有多少数字（不超过五个）：");
    int k = 0;
    scanf_s("%d", &k); // 注意这里应该传入 k 的地址

    if (k > 5 || k <= 0) { // 检查输入是否符合要求
        printf("输入的数量必须大于0且不超过五个。\n");
        return 1; // 返回错误代码
    }

    printf("请输入 %d 个数字：", k);
    int num[5];
    for (int i = 0; i < k; i++) {
        scanf_s("%d", &num[i]); // 需要传入每个元素的地址
    }

    printf("逆序输出为：");
    for (int j = k - 1; j >= 0; j--) { // 修正循环边界
        printf("%d ", num[j]); // 添加空格使输出更清晰
    }
    printf("\n"); // 结束后换行

    return 0;
}
