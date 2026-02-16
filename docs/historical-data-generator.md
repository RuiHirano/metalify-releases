# (オプション) ヒストリカルデータを生成する

ヒストリカルデータ生成機能は、Axioryの1分足（M1）データをもとに、MT4オフラインチャート用のヒストリカルデータ（HSTファイル）を自動生成する機能です。

## 概要

この機能では以下の作業を自動で行います：

1. AxioryのM1ヒストリカルデータをクラウドからダウンロード
2. 指定した時間足（M5、M15、H1など）に自動集約
3. MT4のオフラインチャートで使用できるHSTファイルを生成
4. MT4の履歴フォルダに自動配置

> [!NOTE]
> データの品質や正確性はAxioryの提供データに依存します。

## 前提条件

ヒストリカルデータを生成する前に、以下の設定が必要です：

### MT4データフォルダの設定

1. Metalify Controllerアプリで右上のメニューから「設定」を開きます
2. 「MT4データフォルダ設定」にMT4のデータフォルダパスを入力します
   - MT4の「ファイル」→「データフォルダを開く」から確認できます
   - 例：`C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx`

![AltText {priority}{768x432}](/img/app_settings.ja.png)

> [!WARNING]
> MT4データフォルダが未設定の場合、ヒストリカルデータ生成ダイアログに警告が表示され、生成ができません。

## 使い方

### 1. ヒストリカルデータ生成ダイアログを開く

Metalify Controllerアプリの右上メニューから「ヒストリカルデータ生成」をクリックします。

![AltText {priority}{768x432}](/img/historical-data-open-dialog.ja.png)

### 2. サーバー名を選択

MT4サーバー名を選択または入力します。

- ドロップダウンリストから既存のサーバー名を選択できます
- リストにない場合は手動で入力することもできます
- 例：`Default`, `FXDD-MT4 Demo Server`, `Axiory-Demo`

![AltText {priority}{768x432}](/img/historical-data-server-select.ja.png)

> [!TIP]
> サーバー名は、生成されるHSTファイルの保存先を決定します。MT4で使用しているサーバー名と一致させてください。

### 3. 通貨ペア（シンボル）を選択

ドロップダウンから通貨ペアを選択します。

利用可能な通貨ペア：

- **メジャー通貨ペア**：EURUSD、USDJPY、GBPUSD、USDCHFなど
- **クロス通貨ペア**：EURJPY、GBPJPY、AUDJPY、EURGBPなど
- **貴金属**：XAUUSD（金）、XAGUSD（銀）

![AltText {priority}{768x432}](/img/historical-data-symbol-select.ja.png)

### 4. 期間を設定

データをダウンロードする期間を指定します。

- **開始年**：2015年〜2025年から選択
- **終了年**：2015年〜2025年から選択

例：2020年から2025年のデータが必要な場合

- 開始年：2020
- 終了年：2025

![AltText {priority}{768x432}](/img/historical-data-period-select.ja.png)

> [!NOTE]
> 期間が長いほど、ダウンロードと生成に時間がかかります。

### 5. 生成する時間足を選択

生成したい時間足にチェックを入れます。

利用可能な時間足：

- M1（1分足）
- M5（5分足）
- M15（15分足）
- M30（30分足）
- H1（1時間足）
- H4（4時間足）
- D1（日足）
- W1（週足）
- MN1（月足）

便利な機能：

- 「すべて選択」：全ての時間足を一括選択
- 「すべて解除」：全ての選択を一括解除

![AltText {priority}{768x432}](/img/historical-data-timeframe-select.ja.png)

> [!TIP]
> バックテストで使用する時間足のみを選択することで、生成時間を短縮できます。

### 6. 生成を開始

「生成」ボタンをクリックすると、ヒストリカルデータの生成が開始されます。

生成中は青色の進行中メッセージが表示されます。

### 7. 生成完了

生成が完了すると、緑色の成功メッセージが表示されます。

- 生成されたHSTファイルの一覧が表示されます
- 「履歴フォルダを開く」ボタンをクリックすると、生成されたファイルの保存場所が開きます

![AltText {priority}{768x432}](/img/historical-data-success.ja.png)

## 生成されるファイル

ヒストリカルデータは以下のパスに保存されます：

```
[MT4データフォルダ]/history/[サーバー名]/[シンボル]-GEN[時間足].hst
```

例：

- サーバー名：`Default`
- シンボル：`EURUSD`
- 時間足：M5、H1、D1を選択

生成されるファイル：

```
C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx\history\Default\EURUSD-GENM5.hst
C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx\history\Default\EURUSD-GENH1.hst
C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx\history\Default\EURUSD-GEND1.hst
```

> [!NOTE]
> シンボル名に`-GEN`サフィックスが自動的に追加されます。

これでヒストリカルデータの生成は完了です！生成されたデータを使用して、MT4のオフラインチャートでバックテストを実行できます。バックテストの詳しい手順については、[バックテストの進め方](/docs/how-to-backtest)をご覧ください。
