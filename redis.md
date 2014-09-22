# redis的数据结构
redis支持五种数据结构: ``STRINGs``, ``LISTs``, ``SETs``, ``HASHes``, ``ZSETs``。

五种数据结构都有一些公用的命令(``DEL``,``TYPE``,``RENAME``等等)。

``STRINGs``,``LISTs``和``HASHes``的实现语义和绝大多数编程语言一致。一些编程语言可能有``set``类型，和redis中的``SETs``一致。``ZSETs``在redis中有些独特，但是很容易使用。

## redis五种数据结构对照表
| 结构类型 | 可包含数据类型 | 结构读/写方式 |
| -- | -- | -- |
| STRING | 字符串，整型或浮点型数值 | 对整个或部分字符串操作，增减整数和浮点数 |
| LIST | 字符串链表 | 可从两端弹出或压入数据，基于坐标截取，读取单个或多个项，按值查找或删除键 |
| SET | 无序不重复字符串的集合 | 增加，获取或删除单个项，检测成员关系，交、并、差操作，获取随机项 |
| HASH | 无序键值对哈希表 | 增加，获取或删除单个项，获取整个hash |
| ZSET(sorted set) | 按数值大小排序的映射 | 增加，获取或删除单个值，获取基于值范围或成员值的项 |
