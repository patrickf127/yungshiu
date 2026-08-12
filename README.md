# 安聯人壽智能客服 AI Agent

一個以 Web 技術建置的 AI 智能客服實作專案，透過 JavaScript 串接 n8n Workflow，結合 RAG（Retrieval-Augmented Generation）知識檢索，讓使用者可以透過自然語言詢問保險相關問題。

本專案使用 **Claude Code / Vibe Coding** 輔助開發，實作前端介面、API 串接、n8n Workflow、RAG 與 AI Agent 整合。

## 🌐 Demo

前端網站：

https://patrickf127.github.io/yungshiu/

GitHub Repository：

https://github.com/patrickf127/yungshiu

> Demo 前端部署於 GitHub Pages，AI 後端 Workflow 運行於本機 n8n，透過 ngrok 建立 HTTPS Tunnel 提供遠端 API 存取。

---

## ✨ 主要功能

- AI 智能客服對話介面
- 自然語言問答
- RAG 知識庫檢索
- n8n Workflow 自動化
- Webhook API 串接
- 遠端 Web 前端連接本機 AI Workflow
- AI 生成客服回覆
- Responsive Web Interface

---

## 🏗️ 系統架構

```text
┌──────────────────────┐
│      使用者瀏覽器      │
└──────────┬───────────┘
           │
           │ HTTPS
           ▼
┌──────────────────────┐
│     GitHub Pages     │
│   HTML / JavaScript  │
└──────────┬───────────┘
           │
           │ API Request
           ▼
┌──────────────────────┐
│        ngrok         │
│    HTTPS Tunnel      │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│      Local n8n       │
│    Webhook Trigger   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│      RAG Workflow    │
│ Knowledge Retrieval  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│       LLM / AI       │
│    Generate Answer   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│      AI 回覆結果      │
│   返回 Web 客服介面   │
└──────────────────────┘
