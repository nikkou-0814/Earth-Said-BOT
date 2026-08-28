# EarthSaid

> [!WARNING]
>## このプロジェクトは開発が終了しています！
> 以降アップデートはされません。
> 
> また、正しく動作する保証もありません。

<div style="text-align: center;">
    <img src="screenshot.png" alt="Discord Screenshot" style="max-width: 100%; height: auto;">
</div>
※現在のものではありません

## 環境構築

> [!WARNING]
> python3 がインストールされている前提です。

### クローン

GitHub からリポジトリをクローンします。

```bash
git clone https://github.com/nikkou-0814/Earth-Said-BOT.git
```

### 環境変数

1. .env.exampleファイルをコピーします。

2. ファイル名を`.env`に変更

2. Discord BOT のトークンとチャンネルIDを記載します。

```env
TOKEN=<DISOCRD_TOKEN>

ChannelID=<DISCORD_ChannelID>
```

## 依存関係のインストールと起動

```bash
pip install -r requirements.txt
```
```bash
python bot.py
```

## 情報送信条件
### 使用方法
`.env`に以下を追加
```env
ForecastWarning=<Forecast,Warning,All>
```

`Forecast`、`Warning`、`All`から一つ選択

### Forecast

`Forecast`の場合は緊急地震速報（予報）のみ送信します。

### Warning

`Warning`の場合は緊急地震速報（警報）のみ送信します。

### All

`All`の場合はすべての緊急地震速報を送信します。

## 震源やマグニチュードの精度情報
`.env`に以下を追加
```env
AccuracyBoolean=<Boolean>
```
`True`または`False`から選択
### True
`True`の場合は震源の精度、深さの精度、マグニチュードの精度をEEWのメッセージに追加します。

### False
`False`の場合は震源の精度、深さの精度、マグニチュードの精度をEEWのメッセージに追加しません。

## 注意
このリポジトリを使用する際に発生した<ins>損害については、開発者は一切責任を負いません</ins>。十分に注意してご利用ください。

> [!WARNING]
>## テストデータに関する注意
>テストデータは2024年6月3日午前6時31分頃発生した石川県能登地方を震源とする最大震度5強を観測した地震のデータです。
>
>テストデータは本来開発をしやすくする目的で導入しています。（```@silent```でのメッセージするようにしています。）
>
>このリポジトリ内のプログラムを改造してテストデータであることを知らせる記述を削除し、
>サーバーメンバーを混乱させる行為などは絶対にしないでください。

## 謝礼

- 地震情報API > P2PQuake JSON API v2
- 緊急地震API > Wolfx API
- テストデータ > dmdata.jp 緊急地震速報イベント一覧 より一部改変
