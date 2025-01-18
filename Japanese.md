# Minaで最初のzkAppを作成する

ブロックチェーンの神秘的な世界で、プライバシーはウィリー・ウォンカの工場への黄金のチケットよりも貴重です。その世界にはMinaというプロトコルがあります。ゼロ知識証明（zk-SNARKs）の謎めいた魔法の力で動くMinaは、あなたの元カレのコミットメント問題よりも軽いブロックチェーンを誇ります。ここではアプリを構築するだけではありません。プライバシーを重視し、高いガス代を嫌う**zkApp**スマートコントラクトを作り出すのです。

![mina1-modified](https://github.com/user-attachments/assets/42d36f97-48e7-44a1-a201-937ce0b360f4)
---

## 冒険の始まり：Minaの魔法を理解する

取引があなたの最後の関係の終わりよりも速く、ガス代が平らな地球説信者の夢のように低いブロックチェーンを想像してください。これがMinaの世界です。ここでは、オフチェーン計算によってプロセスではなく証明の分だけ支払います。


---

## 冒険の準備：必要なもの

- **zkApp CLI**：この冒険のための魔法の杖  
- **TypeScript**：JavaScriptが成長した姿  
- **Node.js (v18+), npm (v10+), git (v2+)**：現代の魔術師の基本ツールキット  

> **プロのヒント**：インストール後に端末をリロードするのを忘れないでください。魔法の呪文が誤作動しないように！

---

## 2つの道：o1js か Protokit か？
![mina2-modified](https://github.com/user-attachments/assets/b58e3bbb-0b5f-436b-956a-5b91741dde77)
---

## **o1js - 初心者向けのエリクサー**

![mina0-modified](https://github.com/user-attachments/assets/ef34c816-5ce8-46dc-b3f9-63f05f333a5e)

o1jsは、あなたに魔法の基礎を教えてくれるフレンドリーな魔術師のようなものです。TypeScriptベースで、あなたのお気に入りのブランケットのように安心感を与えます。

#### o1jsを使用する手順：
1. **CLIをインストール**:  
   ```bash
   npm install -g zkapp-cli
   zk --version  # 魔法の杖が準備できているか確認
   zk project あなたのプロジェクト名  # 魔法の書を作成
   ```
2. **ナビゲート**: 作成したプロジェクトに移動  
   ```bash
   cd あなたのプロジェクト名
   ```
3. **テストとビルド**:  
   ```bash
   npm run test
   npm run build
   npm run start
   ```
4. **デプロイ**:  
   ```bash
   zk config  # 設定
   zk deploy  # zkAppを展開
   ```

#### 使用例：
数独パズルや○×ゲームなど、o1jsは汎用的なzk回路のプレイグラウンドです。

#### o1jsを使用するタイミング：
プロジェクトの状態管理が**オンチェーンの8つのフィールド要素以内**に収まる場合、o1jsが適しています。それ以上の容量が必要な場合、オフチェーンストレージAPIを検討する必要があります。

[「o1jsを使用したzkApp開発の方法」](https://docs.minaprotocol.com/zkapps/o1js)を参照。

---

## **Protokit - 上級者向けの魔術師の選択**

![mina3-modified](https://github.com/user-attachments/assets/53471822-5880-46e2-8ff2-4abdbb44deba)


Solidityに馴染みがある人にとって、Protokitはプライバシー魔法が加わった馴染み深い呪文書のように感じるでしょう。

#### Protokitを使用する手順：
1. **スターターキットをクローン**:  
   ```bash
   git clone https://github.com/proto-kit/starter-kit my-chain
   cd my-chain
   nvm use
   pnpm install
   ```
2. **テスト**:  
   ```bash
   pnpm run test --filter=chain
   ```
3. **チェーンを起動**:  
   ```bash
   pnpm env:inmemory dev --filter chain  # シーケンサー
   pnpm env:inmemory dev --filter web  # UI
   ```
4. **インタラクション**: `localhost:3000`を開き、Auroウォレットを設定してトークンを請求します。

![mina4-modified](https://github.com/user-attachments/assets/b8ad5887-087c-4071-9016-ea1ddd5a9bcb)

[詳細はこちら](https://protokit.dev/docs/quickstart)

---

## セキュリティに関する注意点 - スクロールを守る

この世界ではセキュリティは鍵をかける以上のものです。以下を心に留めてください：
- 論理は証明の中に収めること  
- o1jsをだまそうとしない  
- 誰も信用しないこと  

---

## 最後に

TypeScriptの深淵からプライバシーに重点を置いたブロックチェーンアプリケーションの頂点まで、MinaでのzkApp作成の旅を終えました。**プライバシーは守るべきドラゴン**であり、zkAppはその盾です。

### さらなる情報：
- [zkAppsフレームワーク](https://docs.minaprotocol.com/zkapps/zkapp-development-frameworks)
- [zkプログラミングの基本](https://docs.minaprotocol.com/zkapps/o1js/basic-concepts)
