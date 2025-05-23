# Fast-API-study
FastAPI入門


## コマンド

### 起動

```bash
docker compose up
```

http://localhost:8000/docs にアクセスすることでswaggerが見れる

### ライブラリインストール
```bash
docker compose exec demo-app poetry add ライブラリ名 
```

### DBコンテナ
```bash
docker compose exec db mysql fastapi_study
```

### DBマイグレーション
```bash
docker compose exec demo-app poetry run python -m api.migrate_db 
```

### テスト

```bash
docker compose run --entrypoint "poetry run pytest --asyncio-mode=auto" demo-app
```