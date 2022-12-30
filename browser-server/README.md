# 交付文档

代码
- github repo https://github.com/node-plus/browser-server/tree/1-new-interface

已部署api
- API地址 https://platon-api-test.nodeplus.io/browser-server/
- swagger地址 https://platon-api-test.nodeplus.io/browser-server/#/home


## 文档说明
### 测试文档

| File                                                  | Description |
|-------------------------------------------------------|-------------|
| Nodeplus API Test Collections.postman_collection.json | postman测试工具，包括已配置好的测试用例       |
| 待核实sql                                             | 测试用例文档中跟sql相关的改动            |
| 接口测试用例.xlsx                                     | 测试用例及待核实列表            |
| 项目架构文档                                          | 项目架构，及安装部署文档            |


## 待核实问题总结
### 新增接口
1. swagger文档说明跟实际api不符合
2. 根据文档描述实现接口，但是逻辑有疑问
- 2.2.2 节点历史年化率   avg min max ， 依据文档描述来实现的话，逻辑可能不合理
3. nodeid参数校验, 非法字符预期应该报400, 需确认nodeid regex规范

### 原始接口
1. 交易类型的分析  1159 和 721 数据处理有疑问，历史数据似乎没有处理
2. 内置地址数据在文档中遗漏
3. redis导致的数据不一致问题，不会从数据库加载
4. 文档说明和实际实现不符合
