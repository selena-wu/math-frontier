# Mathematical Frontier

网站：https://selena-wu.github.io/math-frontier/

## 首次发布
仓库 Settings → Pages → Source 选择 Deploy from a branch → main → / (root) → Save。

## 修改首页、About 和联系方式
打开 content/profile.json → 点击铅笔编辑。只修改引号内的文字，保留逗号、双引号和括号。换行用 \n。保存时点击 Commit changes。
字段：brand 导航简称，name 首页标题，bio 简介，welcome 欢迎语，caption 补充说明，about About 正文，contactEmail 邮箱，contactWeChat 微信。
About 中 ## 表示段落标题，{{contact}} 自动显示联系方式。

## 修改头像
在 assets 目录上传新 avatar.png，替换原图。也可上传不同文件名，然后修改 profile.json 的 avatar 路径。

## 添加文章、笔记或播客
在 files 目录上传 PDF 或较小的 MP3；大音频可填写外部 HTTPS 音频直链。
编辑 content/entries.json，在数组内新增一个对象，各对象之间用逗号分隔：

```json
{
  "id": "my-first-note",
  "kind": "note",
  "title": "笔记标题",
  "summary": "简短介绍",
  "content": "正文第一段\n\n正文第二段",
  "topic": "Real Analysis",
  "date": "2026-10-09",
  "attachment": "files/my-note.pdf",
  "file_name": "下载笔记 PDF",
  "status": "published"
}
```

kind：note = Projects & Notes，writing = Writing，podcast = Podcast。
没有附件时 attachment 和 file_name 填空字符串。id 必须唯一。
所有修改提交后会自动重新发布，等部署完成再刷新网页。

## 公开内容与编辑方式
这是 GitHub Pages 静态网站，通过 GitHub 编辑和上传文件。未迁移原站的 ChatGPT 登录或数据库后台。
仓库公开：不要上传私密资料、密码或未公开草稿。即使 status 写 draft，仓库文件仍是公开的。
