## 成语接龙

### 主要功能点

v1.0

- 成语搜索
  - 首字搜索
  - 非首字搜索
  - 同字搜索
  - 同音搜索
- 成语接龙

v2.0

- 成语解释
- 成语拼音
- 成语接龙历史记录

### 实现步骤

- 主界面只有 2 个按钮，查成语/玩接龙
- 查成语
  - 进入搜索界面
  - 可供选择首字或非首字查找，默认首字查找
  - 可供选择同字或同音查找，默认同字查找
- 玩接龙
  - 进入接龙界面，机器人取名为小龙
  - 弹窗选择谁先开始
  - 将 idiom 遍历，把每个成语第一个字都转换为拼音,然后写入一个键值对，key 为拼音，value 为对应的成语数组
  - 若小龙先开始
    - 取一个随机数做 index，取 idiom[index]开始
  - 若玩家先开始
    - 输入框自由填写
  - 游戏规则
    - 如果是玩家输入的话，是否第一个接龙词
      - 如果是，则继续
      - 如果不是，需要检查输入的第一个字是否是上一个的末尾音，即把上一个词最后一个字和输入的第一个字转为拼音对比，相等即继续
    - 玩家输入的值放入 idiom 中遍历，如果没有遍历出来则提示输入的不是成语
    - 是成语的话取最后一个字，在 idiom 中过滤以这个字开头的成语，然后随机返回一个
    - 如果相同的汉字在 idiom 中没有的话，将这个字转换成拼音，在键值对中随机一个

## 其他相关功能

- 古诗词 飞花令
- 歇后语
- 押韵 韵脚
