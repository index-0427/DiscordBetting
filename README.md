# DiscordBetting

Discord上で賭けイベントを開催するBot。[inoue-773/DiscordBetting](https://github.com/inoue-773/DiscordBetting) のフォーク。

## セットアップ

```
cp .env.example .env  # トークン等を記入
docker build -t discord-betting .
docker run -d --name discord-betting --restart unless-stopped discord-betting
```

### .env

| 変数 | 説明 |
|------|------|
| `DISCORD_BOT_TOKEN` | Discord Botトークン |
| `MONGODB_CLUSTER_LINK` | MongoDB接続URI |
| `ADMIN_ROLE_ID` | 管理者ロールID（カンマ区切りで複数指定可） |
| `DISTRIBUTED_PERCENTAGE` | 勝者への分配率（0.0〜1.0） |

## コマンド

| コマンド | 説明 | 権限 |
|----------|------|------|
| `/start` | 賭けを開始 | 管理者 |
| `/bet` | 対戦者に賭ける | 全員 |
| `/close` | 賭けを締め切る | 管理者 |
| `/winner` | 勝者を決定し払い戻し | 管理者 |
| `/refund` | 全額返金して中断 | 管理者 |
| `/pts` | 自分の所持ポイント確認 | 全員 |
| `/addpt` | ポイントを付与 | 管理者 |
| `/reducept` | ポイントを減らす | 管理者 |
| `/leaderboard` | 1pt以上の保有者一覧と総額 | 管理者 |
| `/balance` | 特定ユーザーのポイント確認 | 管理者 |

## ライセンス

フォーク元のコードの利用許諾は [inoue-773](https://github.com/inoue-773) に確認してください。

本フォークで追加・変更した部分は MIT License で提供します。自由にご利用ください。
