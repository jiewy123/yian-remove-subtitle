# 宜安去字幕 - Vercel 后端 API

## 部署方法

### 方法 1：Vercel CLI（推荐）

```bash
# 1. 安装 Vercel CLI
npm i -g vercel

# 2. 进入项目目录
cd vercel-api

# 3. 登录并部署
vercel login
vercel
```

### 方法 2：GitHub 部署

1. 上传代码到 GitHub
2. 访问 https://vercel.com
3. Import GitHub 仓库
4. 自动部署

## API 接口

| 接口 | 方法 | 说明 |
|------|------|------|
| `/api/health` | GET | 健康检查 |
| `/api/video/process` | POST | 处理视频 |
| `/api/video/status/<task_id>` | GET | 查询状态 |

## 注意

⚠️ Vercel 免费版不适合处理大视频：
- 请求大小限制：4MB
- 函数执行时间：10秒

**如需处理大视频，需要：**
1. 升级付费版
2. 或结合云存储 + 第三方视频处理服务

## 本地运行

```bash
pip install -r requirements.txt
python api/app.py
```