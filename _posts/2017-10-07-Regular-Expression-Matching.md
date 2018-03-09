---
layout: post
title: "Regular Expression Matching"
description: Leetcode Solution.
image: 'https://wx2.sinaimg.cn/mw690/d63ab74bly1fp6fjloawkj20l30flnay.jpg'
category: 'blog'
tags:
- c++
- leetcode
twitter_text: 正则表达式匹配.
introduction: 正则表达式匹配.
---

# [Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/) 题解
[TOC]

------

## 题目描述
![Regular Expression Matching](https://i1.hdslb.com/bfs/archive/1cf17d0b411ab244f811c145dd646c3db0af93b6.jpg "Regular Expression Matching")
即判断字符串与正则表达式(只支持'.'和'\*')是否匹配。
如："abab"与".\*..ab"返回true。

## 题解
因为元字符'\*'可以匹配的数量不定，最长匹配或最短匹配都无法适应，所以只能通过一个容器记录转移状态。类似于状态转移图，所以简单两层循环即可。外循环遍历字符串，内循环寻找匹配的下一个状态。当最终完成遍历且最后状态中有两字符串最后匹配状态即匹配成功，反之失败。


## 代码

```cpp
class Solution {
public:
    bool isMatch(std::string s, std::string p) {
        size_t lenS = s.size(), lenP = p.size();
        std::vector<int> vec;
        vec.push_back(0);
        for (int j = 0; j < lenP;) {
            std::vector<int> tmpVec;
            char cur = p[j];
            if (j + 1 < lenP && p[j + 1] == '*') {
                if (vec.size()) {
                    if (cur == '.') {
                        for (size_t k = vec[0]; k <= lenS; ++k)
                            tmpVec.push_back(k);
                    } else {
                        int tmpLen = vec.size() - 1;
                        for (int k = 0; k < tmpLen; ++k) {
                            int end = vec[k + 1];
                            for (int i = vec[k]; i < end; ++i) {
                                tmpVec.push_back(i);
                                if (cur != s[i])
                                    break;
                            }
                        }
                        for (int i = vec[tmpLen]; ; ++i) {
                            tmpVec.push_back(i);
                            if (i == lenS || cur != s[i])
                                break;
                        }
                    }
                }
                j += 2;
            } else {
                for (size_t k = 0; k < vec.size(); ++k)
                    if (vec[k] < lenS && (cur == '.' || cur == s[vec[k]]))
                        tmpVec.push_back(vec[k] + 1);
                ++j;
            }
            if (tmpVec.empty())
                return false;
            vec = tmpVec;
        }
        return vec.size() && vec.back() == lenS;
    }
};
```

## 总结
主要应用了状态转移图思想。
