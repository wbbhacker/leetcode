## 分数排名
### 题目描述

编写一个 SQL 查询来实现分数排名。如果两个分数相同，则两个分数排名（Rank）相同。请注意，平分后的下一个名次应该是下一个连续的整数值。换句话说，名次之间不应该有“间隔”。
```
+----+-------+
| Id | Score |
+----+-------+
| 1  | 3.50  |
| 2  | 3.65  |
| 3  | 4.00  |
| 4  | 3.85  |
| 5  | 4.00  |
| 6  | 3.65  |
+----+-------+
```

例如，根据上述给定的 `Scores` 表，你的查询应该返回（按分数从高到低排列）：
```
+-------+------+
| Score | Rank |
+-------+------+
| 4.00  | 1    |
| 4.00  | 1    |
| 3.85  | 2    |
| 3.65  | 3    |
| 3.65  | 3    |
| 3.50  | 4    |
+-------+------+
```

### 解法
对于每一个分数，找出表中有多少个 `>=` 该分数的不同的(distinct)分数，然后按降序排列。

```sql
# Write your MySQL query statement below

select Score, (select count(distinct Score) from Scores where Score >= s.Score) Rank from Scores s order by Score desc;

```

#### Input
```json
{
    "headers": {
        "Scores": [
            "Id",
            "Score"
        ]
    },
    "rows": {
        "Scores": [
            [
                1,
                3.50
            ],
            [
                2,
                3.65
            ],
            [
                3,
                4.00
            ],
            [
                4,
                3.85
            ],
            [
                5,
                4.00
            ],
            [
                6,
                3.65
            ]
        ]
    }
}
```

#### Output
```json
{
    "headers": [
        "Score",
        "Rank"
    ],
    "values": [
        [
            4.0,
            1
        ],
        [
            4.0,
            1
        ],
        [
            3.85,
            2
        ],
        [
            3.65,
            3
        ],
        [
            3.65,
            3
        ],
        [
            3.5,
            4
        ]
    ]
}
```

# [题目](这里是题目链接，如：https://leetcode-cn.com/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof/)

## 题目描述
<!-- 这里写题目描述 -->


## 解法
<!-- 这里可写通用的实现逻辑 -->


### Python3
<!-- 这里可写当前语言的特殊实现逻辑 -->

```python

```

### Java
<!-- 这里可写当前语言的特殊实现逻辑 -->

```java

```

### ...
```

```