# 洛克王国手游随机抽选与对战系统

一个静态网页工具，用于从洛克王国手游精灵池中随机抽选精灵，并管理赛事对战流程。

![页面示例](https://github.com/user-attachments/assets/8f08b7c7-7eb2-450f-a4bb-0368c47b1263)

## 在线使用

- 随机抽选页：https://tortes.github.io/RocoTournament/
- 对战系统页：https://tortes.github.io/RocoTournament/tournament.html

## 功能

- 一键随机抽选 6 只精灵并展示图片。
- 支持查看历史抽选结果。
- 随机池仅包含一阶精灵和一阶地区主形态，排除首领与传说精灵。
- 对战系统支持录入参赛人员、本地保存、随机 roll 6 只精灵。
- 手动填入精灵不做随机池限制，可填写任意编号或名称。
- 支持两组小组赛、手动录入胜场和剩余精灵数量。
- 支持进入淘汰赛、决赛和季军赛，并手动选择胜者。

## 本地启动

由于对战页会读取 `index.html` 中的精灵池数据，建议通过本地 HTTP 服务访问：

```bash
python3 -m http.server 4173
```

然后打开：

```text
http://127.0.0.1:4173/
http://127.0.0.1:4173/tournament.html
```

## 文件说明

- `index.html`：随机抽选页。
- `tournament.html`：对战系统页。
- `dex-data.js`：完整图鉴头像数据，用于对战页手动输入精灵时匹配头像。
- `excluded-lists.md`：当前随机池排除列表记录。
