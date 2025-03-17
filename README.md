# diary-app-frontend
<<<<<<< develop

## **プロジェクト概要**
本プロジェクトは、日記管理アプリのフロントエンドです。Vue.js と Vite を使用して構築されており、バックエンド（Spring Boot）と連携して日記の作成・編集・削除・一覧表示を行います。

## **環境構築**

### **必要なツール**
- **Node.js**（推奨バージョン: 16 以上）
- **npm**（Node.js に付属）

### **インストール手順**
1. **リポジトリをクローン**
   ```sh
   git clone <リポジトリURL>
   cd diary-app-frontend
   ```
2. **依存パッケージをインストール**
   ```sh
   npm install
   ```
3. **開発サーバーを起動**
   ```sh
   npm run dev
   ```
4. **ブラウザでアクセス**
   - `http://localhost:5173/`

## **プロジェクト構成**
```sh
diary-app-frontend/
├── node_modules/        # 依存パッケージ
├── public/              # 静的ファイル
├── src/                 # ソースコード
│   ├── assets/         # 画像、CSS などの静的ファイル
│   ├── components/     # Vue コンポーネント
│   ├── views/          # ページ単位のコンポーネント
│   ├── router/         # ルーティング設定
│   ├── store/          # 状態管理（Vuex, Pinia）
│   ├── App.vue         # ルートコンポーネント
│   ├── main.js         # エントリーポイント
├── index.html           # HTML エントリーポイント
├── package.json         # 依存パッケージ情報
├── vite.config.js       # Vite 設定
└── README.md            # 本ファイル
```

## **主要機能**
- **日記一覧の表示** (`GET /api/diaries`)
- **日記の作成** (`POST /api/diaries`)
- **日記の編集** (`PUT /api/diaries/{id}`)
- **日記の削除** (`DELETE /api/diaries/{id}`)

## **API との連携**
バックエンドの API（Spring Boot）と通信するために `axios` を使用。

### **`axios` のインストール**
```sh
npm install axios
```

### **API 呼び出しの例（`DiaryList.vue`）**
```javascript
import axios from "axios";
export default {
  data() {
    return {
      diaries: []
    };
  },
  mounted() {
    axios.get("http://localhost:8080/api/diaries")
      .then(response => {
        this.diaries = response.data;
      })
      .catch(error => {
        console.error("APIエラー:", error);
      });
  }
};
```

## **開発コマンド**
| **コマンド** | **説明** |
|----------|------------------|
| `npm install` | 依存パッケージのインストール |
| `npm run dev` | 開発サーバーの起動 |
| `npm run build` | 本番環境用にビルド |
| `npm run preview` | ビルド後のプレビュー |

## **注意点**
- **バックエンド（`diary-app-backend`）を起動してからフロントエンドを実行すること。**
- **CORS 設定が正しく行われていることを確認。**


=======

## **プロジェクト概要**
本プロジェクトは、日記管理アプリのフロントエンドです。Vue.js と Vite を使用して構築されており、バックエンド（Spring Boot）と連携して日記の作成・編集・削除・一覧表示を行います。

## **環境構築**

### **必要なツール**
- **Node.js**（推奨バージョン: 16 以上）
- **npm**（Node.js に付属）

### **インストール手順**
1. **リポジトリをクローン**
   ```sh
   git clone <リポジトリURL>
   cd diary-app-frontend
   ```
2. **依存パッケージをインストール**
   ```sh
   npm install
   ```
3. **開発サーバーを起動**
   ```sh
   npm run dev
   ```
4. **ブラウザでアクセス**
   - `http://localhost:5173/`

## **プロジェクト構成**
```sh
diary-app-frontend/
├── node_modules/        # 依存パッケージ
├── public/              # 静的ファイル
├── src/                 # ソースコード
│   ├── assets/         # 画像、CSS などの静的ファイル
│   ├── components/     # Vue コンポーネント
│   ├── views/          # ページ単位のコンポーネント
│   ├── router/         # ルーティング設定
│   ├── store/          # 状態管理（Vuex, Pinia）
│   ├── App.vue         # ルートコンポーネント
│   ├── main.js         # エントリーポイント
├── index.html           # HTML エントリーポイント
├── package.json         # 依存パッケージ情報
├── vite.config.js       # Vite 設定
└── README.md            # 本ファイル
```

## **主要機能**
- **日記一覧の表示** (`GET /api/diaries`)
- **日記の作成** (`POST /api/diaries`)
- **日記の編集** (`PUT /api/diaries/{id}`)
- **日記の削除** (`DELETE /api/diaries/{id}`)

## **API との連携**
バックエンドの API（Spring Boot）と通信するために `axios` を使用。

### **`axios` のインストール**
```sh
npm install axios
```

### **API 呼び出しの例（`DiaryList.vue`）**
```javascript
import axios from "axios";
export default {
  data() {
    return {
      diaries: []
    };
  },
  mounted() {
    axios.get("http://localhost:8080/api/diaries")
      .then(response => {
        this.diaries = response.data;
      })
      .catch(error => {
        console.error("APIエラー:", error);
      });
  }
};
```

## **開発コマンド**
| **コマンド** | **説明** |
|----------|------------------|
| `npm install` | 依存パッケージのインストール |
| `npm run dev` | 開発サーバーの起動 |
| `npm run build` | 本番環境用にビルド |
| `npm run preview` | ビルド後のプレビュー |

## **注意点**
- **バックエンド（`diary-app-backend`）を起動してからフロントエンドを実行すること。**
- **CORS 設定が正しく行われていることを確認。**
