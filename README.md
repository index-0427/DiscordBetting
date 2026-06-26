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
| `GUIDE_URL` | 賭け方ガイドのURL（任意） |

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
| `/ptlog` | ポイント操作履歴と管理者別統計 | 管理者 |
| `/balance` | 特定ユーザーのポイント確認 | 管理者 |

## License / ライセンスについて

このリポジトリは、[inoue-773](https://github.com/inoue-773)氏らによる DiscordBetting を元にしたフォークです。

フォーク元に由来するソースコードの利用については、フォーク元の権利者による許諾・ライセンス条件に従ってください。
私は、フォーク元に由来するソースコードについて、追加の利用許諾を行うものではありません。

私が新たに作成した部分、および私が追加・改修した部分については、MIT Licenseに基づいて利用していただいて構いません。

私による追加・改修箇所は、フォーク元リポジトリとの差分、コミット履歴、またはファイルの変更履歴を参照して確認してください。
ただし、この許諾はフォーク元に由来するソースコードの利用権を付与するものではありません。
