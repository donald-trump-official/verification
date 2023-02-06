# 验证算法

# 需求

总体目标：验证两个面包板电路连接的等效性，给出错误和警告

具体需求：

1. 从Map对象或JSON字符串读取电路信息
3. 目标电路正确性验证：
   - 检查不完全在面包板上的元件（警告）
   - 检查不可能的连接，如面包板的一个孔中插入多个引脚（错误）
   - 分析连接性，消除位置信息，生成只包含元件连接关系的数据结构（错误）
   - 检查短路元件，包括导线（警告）
4. 目标电路与样本电路一致性验证：
   - 相同的数量和类型（错误）
   - 对应元件参数相同（警告）
   - 连接等效（错误）