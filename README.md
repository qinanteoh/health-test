# 健康营养课 · 顾客健康教育 App

10 天 / 21 天顾客健康教育课程。顾客不用下载 App，用手机号码注册，教练批准后每天解锁一课。

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/qinanteoh/health-course-template)

## 你需要准备
- 一个 **GitHub** 账号（免费）：github.com
- 一个 **Cloudflare** 账号（免费）：dash.cloudflare.com
- 一部电脑（第一次设定用电脑比较方便）

## 建立你自己的 App（大约 10 分钟）
1. 按上面橙色的 **Deploy to Cloudflare** 按钮（就在标题下面）。
2. 用你的 Cloudflare 账号登录，再按提示连接你的 GitHub 账号。
3. 设定页面会出现几栏：
   - **Project name / Worker name**：你的 App 名称，只能用小写英文、数字和横线，例如 `amy-health`。这会变成你的网址的一部分。
   - **D1 database**：资料库，保持默认就可以，系统会自动建立。
   - **ADMIN_PASSWORD**：填你自己的**管理后台密码**，请记下来，不要给别人。
4. 按 **Create and deploy / 部署**，等 1 到 2 分钟。
5. 完成后会给你一个网址，例如 `https://amy-health.你的名称.workers.dev`。

这套 App 是**你自己的**：顾客资料存在你自己的 Cloudflare 里，只有你看得到。

## 开始使用
用上面得到的网址：

| 用途 | 网址 |
|---|---|
| 21 天课程（发给顾客） | `https://amy-health.你的名称.workers.dev` |
| 10 天课程（发给顾客） | 网址后面加 `/10`，例如 `https://amy-health.你的名称.workers.dev/10` |
| 管理后台（你自己用） | 网址后面加 `/admin.html`，输入你的 ADMIN_PASSWORD |

顾客登录画面底下也有「管理员入口」，你从顾客的链接也能进后台。

## 后台怎么用
- **审核新顾客**：顾客注册后会出现在「待审核」，按「批准」他才能开始上课。
- **新申请提醒**：后台开着的时候（放在背景也可以），有人申请会出现橙色提示并响一声。第一次进后台按「开启通知」，手机或电脑也会弹出通知。
- **设定课程**：每个顾客都可以设定「可以看到第几天」和「从第几天开始」。例如 10 天读完的顾客，可以选「21 天 · 从第 11 天开始」，让他直接接着看。
- **回看和重新开通**：读完课程后可以回看 7 天，之后自动关闭。顾客申请重新开通会出现在「申请重开」。
- **浏览统计**：看每天有多少人打开、看了哪几天。

## 把 App 放到手机主画面
用手机打开顾客网址：
- iPhone（Safari）：按分享按钮 → 加入主画面
- Android（Chrome）：按右上角 ⋮ → 加到主画面

## 以后课程有更新时
课程内容更新后，你的 App 不会自动跟着更新。部署时，系统会在你自己的 GitHub 里建立一份这个项目，Cloudflare 会跟着那一份自动重新部署。所以只要把新的档案放进你那一份，App 就会更新，顾客和进度都会保留。

有更新时，给你这个链接的教练会通知你，并告诉你要换哪些档案。

## 档案说明
- `worker.js`：后台程式（注册、登录、审核、课程解锁）
- `public/`：顾客页面、管理后台、图片
- `wrangler.jsonc`：Cloudflare 设定

本课程内容为一般健康教育资讯，不能代替医生的诊断和治疗。
