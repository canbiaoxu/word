# **自由单词・英简中 Wiki 社群词典**

## 项目介绍

开源的英-简中词典仓库，支持学习查询、工具开发、企业集成、在线学习，稳定易用。

仓库地址：[https://github.com/canbiaoxu/word](https://github.com/canbiaoxu/word)

## 单词内容

- 美英双音标。
- 中文释义（按词性分类）。

## 特性

* 单词数据（json）可直接通过URL调用。
* 集成在线学习功能，可在本站网页上学习和记忆单词。

## 单词JSON数据调用

调用单词完整信息：

- url 格式：`https://word.freeing.wiki/groups/{首字母小写}/{单词小写}/word.json`
- 说明：`{首字母小写}`为单词首字母小写（如"clip"用"c"），`{单词小写}`为小写完整单词（如"clip"）。

示例（以"clip"为例）：

- json url：[https://word.freeing.wiki/groups/c/clip/word.json](https://word.freeing.wiki/groups/c/clip/word.json)
- json 内容：

```json
{
    "word": "clip",
    "AmE": "[klɪp]",
    "BrE": "[klɪp]",
    "meanings": {
        "n": [
            "修剪",
            "剪辑，片段",
            "夹子，回形针",
            "速度"
        ],
        "vi": [
            "快速或急促地移动"
        ],
        "vt": [
            "减少，降低",
            "剪辑，修剪",
            "紧紧固定"
        ]
    }
}
```

字段说明：`word`（单词）、`AmE`（美式音标）、`BrE`（美式音标）、`meanings`（中文释义）均为必含项。

## 在线学习

学习方法：

| 方法                                              | 描述                                                                                                                                             |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| [敲单词](https://word.freeing.wiki/study_way/write/) | 采用启发式复习策略，根据用户对具体单词的答题行为智能安排此单词下次出现的时机；集成美英双音频；并集成‘AI释义’功能，实时获取并显示大模型的释义。 |

## 邀请贡献

目前词汇库仍在完善中，欢迎有志之士一起扩充词汇量、修正数据、完善或新增学习方式。

贡献步骤：

1. Fork仓库。
2. 按 `/groups/{首字母小写}/{单词小写}/` 结构新增/修改单词。
3. 提交Commit并推送到你的仓库。
4. 发起PR说明修改内容。

## 鸣谢

本项目在开发或运行过程中主要使用了以下开源软件或API接口，特此感谢！

* [Openai Api](https://platform.openai.com/docs/api-reference/introduction)
* [Pollinations.AI](https://github.com/pollinations/pollinations)

## 更新日志

### v1.1

新增[敲单词](https://word.freeing.wiki/study_way/write/)学习方法。该方法采用启发式复习策略，根据用户对具体单词的答题行为智能安排此单词下次出现的时机；集成美英双音频；并集成‘AI释义’功能，实时获取并显示大模型的释义。

### v1.0

初始版本，上传单词11667个。

单词JSON数据来自ChatGPT-4.0 API，含单词、美英双音标、中文释义。
