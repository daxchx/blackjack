# ブラックジャック

このアプリケーションは、トランプゲームのブラックジャックが遊べるアプリケーションです。

<a href="https://blackjack-neon-nine.vercel.app">🎮アプリケーションを利用してみる</a>

このアプリケーションの使用方法については<a href="/wiki">Wiki</a>をご確認ください。

## プロジェクトの目的

この Project では、ソフトウェア開発において重要な設計（特に MVC）について学習します。

ソフトウェア設計のノウハウを学ぶことで、拡張性の高いコードを書けるようになり、時間と労力を大幅に削減できるようになります。

ここでは Black Jack を MVC に従って実装する過程を学習します。

モデル設計、スケルトン設計などでソフトウェアの設計をしっかりと考えた後、コード化していきます。

このコースを修了すると、ソフトウェアをゼロから開発する基礎力が身につきます。

このプロジェクトでは以下の技術の使用と習得を目的としています。

- オブジェクト指向プログラミング
- MVC アーキテクチャ
- TypeScript
- DOM 操作
- ライブプレイできるゲームの作成

## 役割と貢献
    
このプロジェクトでは以下のことを行いました。

- モデル設計
- スケルトン設計
- デザイン作成
- フロントエンド構築
    
## 技術的な側面
    
このプロジェクトでは以下の技術スタックを採用しています。

### MVCアーキテクチャ

#### 分離された責任

`MVC` は、アプリケーションをモデル（データやビジネスロジック）、ビュー（ユーザーインターフェース）、コントローラ（アプリケーションのフローを制御するロジック）の3つのコンポーネントに分割します。

この分離により、それぞれのコンポーネントは異なる責任を持ち、役割を適切に分離することができます。

#### 保守性と拡張性

`MVC` の分離された構造により、コードがより保守しやすくなり、拡張性が向上します。

たとえば、ビューの変更がモデルやコントローラに影響を与えないため、UIの変更を容易に行うことができます。

#### 再利用性

MVCアーキテクチャでは、コントローラやモデルのロジックを他の部分で再利用することができます。

たとえば、複数のビューが同じデータを表示する場合、同じモデルやコントローラを使用してデータの取得と処理を行うことができます。

テスト容易性: MVCの分離されたコンポーネントは、単体テストや統合テストを容易に行うことができます。モデルやコントローラのロジックを独立してテストすることで、アプリケーションの品質を向上させることができます。

共同開発のサポート: MVCアーキテクチャは、複数の開発者が同時に作業する場合に特に有用です。各コンポーネントの責任が明確に分かれているため、異なる開発者が同じコードベースで作業する際にも、互いの作業が干渉しづらくなります。

これらの理由から、MVCアーキテクチャはWebアプリケーションの開発において広く採用されています。

### オブジェクト指向プログラミング

### TypeScript

MVCアーキテクチャやオブジェクト指向プログラミングにおいて型の指定は重要です。バグを埋め込む要因の排除や開発速度を向上させるという理由で、TypeScriptを採用しました。

### Tailwind CSS

MVCアーキテクチャやオブジェクト指向プログラミングにおいて型の指定は重要です。バグを埋め込む要因の排除や開発速度を向上させるという理由で、TypeScriptを採用しました。

### Vite

**高速な開発体験**: Viteは、開発時におけるリアルタイムな更新を可能にするホットリローディングをサポートしています。これにより、コードの変更を行うたびにブラウザが自動的に更新され、開発者は瞬時に変更の効果を確認できます。

**ES Moduleベースの開発**: Viteは、ES Moduleベースのアプローチを採用しており、モジュールを個別に取得してキャッシュすることで、ビルドやリロードの速度を高めます。これにより、開発者は高速な開発体験を得ることができます。

**プラグインシステム**: Viteは柔軟なプラグインシステムを持っており、ユーザーが必要に応じて機能を追加したり変更したりすることができます。これにより、Viteは個々のプロジェクトのニーズに合わせてカスタマイズすることが可能です。

**パフォーマンスの最適化**: Viteは、本番環境でのバンドル作成時に最適化を施すことができます。モジュールの分割やコードの最適化などの手法を用いて、アプリケーションのパフォーマンスを向上させることができます。

**開発コミュニティの活発さ**: ViteはVue.jsの作者であるEvan Youによって開発されており、Vue.jsコミュニティとの密接な関係を持っています。そのため、Viteを採用することで、強力なサポートや豊富なリソースにアクセスすることができます。

これらの特徴により、Viteは現代のフロントエンド開発において効率的で高速な開発体験を提供し、開発者が柔軟にプロジェクトを構築および管理できるという利点があります。
    
## 問題解決と工夫

MVCアーキテクチャではControllerでそれぞれのオブジェクトの操作を行いました。
ModelとViewが互いに干渉することなく、安全なデータの受け渡しを行うように設計しました。

### オブジェクト指向プログラミング

トランプを使用するブラックジャックでは以下のクラスを用意しました。

<table>
  <tr>
    <th>クラス</th>
    <th>用途</th>
  </tr>
  <tr>
    <td>Table</td>
    <td>テーブルではゲームの進行、プレイヤーの操作、デッキの操作などを行います。</td>
  </tr>
  <tr>
    <td>Player</td>
    <td>手札、賭け金、ステータス、チップなどのデータを保持しています。</td>
  </tr>
  <tr>
    <td>Deck</td>
    <td>複数枚のカードを保持しています。シャッフルやカードをドローなどの操作も可能です。</td>
  </tr>
  <tr>
    <td>Card</td>
    <td>スートやランクなどのカードの情報を保持しています。</td>
  </tr>
  <tr>
    <td>GameDecision</td>
    <td>アクションや賭け金などのプレイヤーの決断を保持します。</td>
  </tr>
</table>

これらのクラスは他のトランプゲームでも使用することができます。

新たにトランプゲームを追加する際にはこれらのクラスを拡張して簡単に追加が可能です。

### DOMの操作

画面全体を再レンダリングすると画像のちらつきや動作が遅くなることがあったため、必要な箇所だけ更新するようにしました。

具体的には、初期化時に必要なdomはすべて用意し、動的な更新が必要なdomにはidを割り振りました。

動的更新を行う際には、controllerからviewのmethodに値を渡し、該当するidの箇所を渡ってきた値を使用して再レンダリングしています。

### MVCアーキテクチャ

<table>
  <tr>
    <th>分類</th>
    <th>クラス</th>
  </tr>
  <tr>
    <td rowspan=5>Model</td>
  </tr>
  <tr>
    <td>Table</td>
  </tr>
  <tr>
    <td>Player</td>
  </tr>
  <tr>
    <td>Deck</td>
  </tr>
  <tr>
    <td>Card</td>
  </tr>
  <tr>
    <td>View</td>
    <td>View</td>
  </tr>
  </tr>
  <tr>
    <td>Controller</td>
    <td>Controller</td>
  </tr>
</table>

ゲームの進行はcontrollerで行いました。

viewとmodelが互いに影響しないようにcontrollerでmodelとviewのインスタンスを生成して操作しています。

### UIデザイン

モダンでシンプルなデザインにして誰でも直感的にプレイできることを意識しました。
レスポンシブデザインにし、スマホでもプレイを楽しむことができるようにしています。

## 学びと成長
    
このプロジェクトを通して以下のような学びや成長がありました。

- MVCアーキテクチャを用いた設計を行えるようになった
- OOPの型の指定がスムーズに行えるようになった
- APIからデータを取得して、処理を実装できるようになった
    
## コードの品質と構造
    
コードの品質についての考え方や重要視する点、プロジェクトのディレクトリ構造やコーディングスタイルについて説明します。

このプロジェクトではオブジェクト指向プログラミングのデザインパターンとしてMVCアーキテクチャを採用しています。

これを採用したことで開発速度の向上と安全なデータの操作が行えています。

コーディングは静的なViewの実装から取り掛かり、Model、Controller、動的なViewの実装という順番で進めていきました。

ディレクトリは以下のようになりました。

- config : 設定ファイル
- interface : オブジェクトの型の指定
- model : コンピュータのデータを定義
- controller : modelとviewの操作を定義
- view : 画面に表示するdomを定義
    
## 今後の展望

このプロジェクトでは、クライアント依存のデータ共有を行っていますが、Supabaseなどのデータベースを使用して、認証機能やユーザー別の情報を保持したアプリケーションの実装も行っていきたいです。

検索した瞬間に簡易的に検索ができる機能を実装したが、特定のキーワードを入力している間に無駄なfetch処理が行われているため、fetch処理が走るまでのバリデーションを設けて、不要なfetchを改善させたい。

このプロジェクトでは、クライアント依存のデータ共有を行っていますが、Supabaseなどのデータベースを使用して、認証機能やユーザー別の情報を保持したアプリケーションの実装も行っていきたいです。
