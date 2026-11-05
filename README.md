# Expense Tracker · 记账

A simple, offline-first budget tracker for iPhone (works in any modern browser).
一个干净、能离线用的记账小工具。

**Open / 打开:** https://rx0825.github.io/expense-tracker/

## Features / 功能

- **Monthly budget & daily limit** — see how much is left this month and how much you can still spend today
  每月预算，显示「本月还剩多少」和「今天还能花多少」
- **Preview before you spend** — type an amount to see what's left after it
  输入金额时，提前显示「记下后还剩多少」
- **Multi-currency** — main currency (USD by default) plus others like CNY; each entry is converted at the rate when it was recorded
  多币种：主要货币 + 其他币种，按记账当时的汇率换算
- **AI expense input** — say or type one sentence ("lunch $12, milk tea ¥25 on WeChat") and AI splits it into entries for you to confirm
  AI 记账：说一句话，AI 拆成几笔，确认后再存
- **Custom categories** — up to 10
  自定义类别（最多 10 个）
- **Works offline** — opens instantly, no internet needed (except for AI)
  离线可用，秒开（AI 功能需要联网）
- **Backup & restore** — export a file to iCloud Drive, import it on a new phone
  备份与恢复
- **Reminders** — nudges you if you haven't recorded in 2+ days or haven't backed up in a week
  很久没记账、没备份时会提醒

## Install on iPhone / 装到 iPhone

1. Open the link above in **Safari**
2. Tap **Share → Add to Home Screen**
3. Always open it from the home screen icon (Safari and the home screen app keep **separate** data)

## Privacy / 隐私

All data stays on your device (browser storage). Nothing is uploaded.
The AI feature sends only the sentence you type to the Anthropic API, using **your own API key**, which is stored only on your device and never included in backups.

所有账目只存在你自己的手机里，不会上传。AI 功能只会把你输入的那句话发给 Anthropic API，用的是你自己的 API key，key 只存在本机，不会进入备份文件。

## Tech

Plain HTML/CSS/JavaScript, no build step. `localStorage` for data, a service worker for offline use.
Built with help from Claude.
