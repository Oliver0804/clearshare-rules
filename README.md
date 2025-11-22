# ClearShare Rules

URL 追蹤參數過濾規則庫，供 [ClearShare](https://github.com/Oliver0804/ClearShare) iOS App 使用。

## 功能

ClearShare App 會自動從這個規則庫同步最新的過濾規則，包括：

- **平台規則**：針對特定網站的參數過濾設定
- **通用追蹤參數**：所有網站都會移除的追蹤參數

## 支援平台

### 社群媒體
- Instagram
- Facebook
- Twitter/X
- Threads
- TikTok
- LinkedIn
- Pinterest
- Reddit

### 影音平台
- YouTube
- Bilibili
- Spotify
- Apple Music
- Netflix

### 電商平台
- 淘寶
- 天貓
- Amazon
- eBay
- AliExpress
- 蝦皮

## 規則格式

```json
{
  "version": "1.0.0",
  "last_updated": "2025-11-23T00:00:00Z",
  "platforms": [
    {
      "name": "平台名稱",
      "domains": ["domain.com"],
      "category": "social|video|ecommerce|media",
      "enabled_by_default": true,
      "filter": {
        "mode": "keep|remove",
        "params": ["param1", "param2"]
      }
    }
  ],
  "common_tracking_params": ["utm_source", "fbclid", "..."]
}
```

### 過濾模式

- **keep**: 只保留指定的參數，移除其他所有參數
- **remove**: 移除指定的參數，保留其他參數

## 貢獻

歡迎提交 PR 來新增或更新規則！

### 新增平台規則

1. Fork 這個 repo
2. 編輯 `rules.json`
3. 在 `platforms` 陣列中新增規則
4. 提交 PR

### 新增追蹤參數

1. Fork 這個 repo
2. 編輯 `rules.json`
3. 在 `common_tracking_params` 陣列中新增參數
4. 提交 PR

## 授權

MIT License

## 作者

BASHCAT ([@Oliver0804](https://github.com/Oliver0804))
