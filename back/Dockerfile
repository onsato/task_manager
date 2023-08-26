# ベースイメージとして公式のNode.jsイメージを使用
FROM node:14

# 作業ディレクトリを設定
WORKDIR /app

# 依存関係のファイルをコピー
COPY package*.json ./

# 依存関係のインストール
RUN npm install

# ソースコードをコピー
COPY . .

# アプリケーションをビルド
RUN npm run build

# ポート3000を公開（NestJSのデフォルトポート）
EXPOSE 3000

# アプリケーションの起動コマンド
CMD ["npm", "start"]
