# 交付文档

代码
- github repo https://github.com/nodeplusio/browser-server/tree/1-new-interface

已部署api
- API地址 https://platon-api.nodeplus.io/browser-server/
- swagger地址 https://platon-api.nodeplus.io/browser-server/#/home


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
> 对应新增接口待核实TestCase编号[001]
2. 根据文档描述实现接口，但是逻辑有疑问
- 2.2.2 节点历史年化率   avg min max ， 依据文档描述来实现的话，逻辑可能不合理
> 对应新增接口待核实TestCase编号[002]
3. nodeid参数校验, 非法字符预期应该报400, 需确认nodeid regex规范
> 对应新增接口待核实TestCase编号[003][004][005][006][007][008]

**更多详情参考 测试文档/接口测试用例.xlsx 中的 "新增接口待核实TestCase" 表格**

### 原始接口
1. 交易类型的分析  1159 和 721 数据处理有疑问，历史数据似乎没有处理
> 对应原有接口待核实TestCase编号[001][002][009][010][016][017]

2. 721 image 地址似乎没有更新历史数据, 导致页面上的图片不能展示
> 对应原有接口待核实TestCase编号[021][022]  
> 示例: 不显示图片的浏览器网页 https://scan.platon.network/tokens-> detail?address=lat13m53valp38lsaq6p234754gau54sdjw0fqymys
> https://static.qpassport.io/resources/images/fireworks/cover/love.gif
> https://static.hashkey.id/resources/images/fireworks/cover/love.gif
3. 部分接口的 pagination 逻辑有问题
> 对应原有接口待核实TestCase编号[020]
4. 内置地址数据在文档中遗漏
> 对应原有接口待核实TestCase编号[004][005][013]
5. token_expand表作为配置表，数据缺失
> 对应原有接口待核实TestCase编号[006][007]
6. redis导致的数据不一致问题，不会从数据库加载
> 对应原有接口待核实TestCase编号[008]
7. 文档说明和实际实现不符合
> 对应原有接口待核实TestCase编号[009][010][012][013]
8. 代码中sql语法报错
> 对应原有接口待核实TestCase编号[014][015]
9. 区块接口，参数校验, 非法字符预期应该报400, 需确认 regex规范
> 对应原有接口待核实TestCase编号[018][019]

**更多详情参考 测试文档/接口测试用例.xlsx 中的 "原有接口待核实TestCase" 表格**
