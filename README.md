# ブラックジャック

## 概要

トランプゲームのブラックジャックが遊べるアプリ

## URL

https://blackjack-neon-nine.vercel.app/

## デモ

以下の動作を gif 装画に集約する

## 説明

このゲームは、トランプゲームのブラックジャックをプレイできます。
ゲーム開始時に各プレイヤーには 400 枚のチップが配布されます。
ラウンド制を取り入れており、設定したラウンドになるまでゲームを続けます。
各ラウンドで、チップを賭けてディーラーとカードの合計値で勝負します。
勝利したプレイヤーは特定の条件下でディーラーからかけたチップに応じたチップを獲得します。
全ラウンドが終了した時点で、各プレイヤーの所持しているチップの枚数を比較してゲームの勝者を決定します。
このゲームは 1 人で遊ぶゲームになっています。あなた以外のプレイヤーの CPU とディーラーは配布されたカードの合計値からアクションを選択して、自動でゲームを進行します。

## 遊び方

1. url にアクセスする
2. プレイするラウンド数を入力する
3. 「start」ボタンをクリックする
4. ベット額を選択する
5. アクションを選択する
6. 「next」をクリックして次のラウンドを開始する
7. 1~6 を繰り返し行い、最後にチップが最も多いプレイヤーの勝利

## ブラックジャックの遊び方

1. 自分のターンが来たら、賭け金を選択しよう
2. カードが配られたら、現在の手札の合計値を確認して、最適なアクションを選択しよう

### アクションリスト

| アクション |                       行動                        |
| :--------: | :-----------------------------------------------: |
| サレンダー |     賭け金の半額をディーラーに渡して降参する      |
|  スタンド  |          手札の状態を確定して勝負に挑む           |
|   ヒット   |            手札にカードを 1 枚追加する            |
|   ダブル   | 　賭け金を 2 倍にして、手札にカードを一枚追加する |

※バースト：手札が 21 を超えたとき、プレイヤーの賭け金はディーラーに回収される

## 使用技術

- TypeScript
- TailwindCSS
- Vite
- Vercel

## クラス図

## アクティビティ図

## UI 一覧

### スタート画面

ここではブラックジャックのラウンド数の選択をします。

### プレイ画面

ここでは

### ベットを選択する場面

### アクションを選択する場面

## 作成の経緯

下記項目の理解を深めるために作成しました。

- OOP
- MVC アーキテクチャ
- typescript
- dom 操作

## こだわった点

#### 設計

拡張性をもたせた設計にしました。
ブラックジャック以外のトランプゲームも容易に追加できるように共通クラスや抽象クラスを作成してします。
また、クラス図やアクティビティ図を使用してブラック・ジャックの動作にバグや実装できていない要件がないようにしました。

#### UI

ワイヤーフレームを作成してユーザーがプレイしやすいようにしました。
モダンでシンプルなデザインにして誰でも直感的にプレイできることを意識しました。
レスポンシブデザインにし、PC でもスマホでもプレイを楽しむことができるようにしています。

## 今後実装したいもの

- 賭け金の増減をわかりやすくする
- ゲームオーバーシーンで全プレイヤーのラウンドログを表示する
