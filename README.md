# 🎯 認清你的朋友 Fun Facts

跨團契合作破冰遊戲。大家秘密寫低一個數字，再靠對團友嘅了解，將箭頭由細至大排好。分數、局數同箭頭位置記喺瀏覽器 localStorage，唔使登入。

## 點玩

1. 揀題庫、回合數，同 3–8 個團友或組別。8–16 人可以幾個人共用一支箭頭。
2. 每人秘密輸入數字並鎖定。可以用右上角「手機秘密寫字板」。
3. 由星星起始玩家開始，其他人輪流將自己支箭頭插入由細至大嘅位置。
4. 起始玩家可以最後移一次自己支箭頭，然後由細至大翻牌。順序啱嘅箭頭每支 +1 分。

## 本機開啟

```bash
python3 -m http.server 8788 --directory public
```

然後開 <http://127.0.0.1:8788>

## 部署

GitHub：https://github.com/Takjai18/fun-facts

靜態檔放喺 `public/`（`index.html`、`questions.json`）。Cloudflare Workers 靜態資源，帳號 Ymtwill。同其他破冰遊戲一樣，唔用 Pages。

```bash
CI=1 npx --yes wrangler@4 deploy
```

線上版：https://fun-facts.ymtwill.workers.dev

## 約書亞主站

Icebreaking 卡片喺 `kyc-joshua` 嘅 `src/pages/index.astro`，`games` 陣列。按鈕用現有粉紅色「開遊戲」。
