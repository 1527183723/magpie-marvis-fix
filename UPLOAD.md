# 上传到 GitHub 说明

这个目录本身就是 `magpie-marvis` 仓库根目录，直接把目录里的全部文件上传到 GitHub 新仓库即可。

## 上传前

- 不要上传 `native/` 下的 `.node` / `.dll` 文件和 `native/qimei36.txt`：这些是从本机 Marvis 客户端提取的二进制和设备指纹，`.gitignore` 已经忽略它们。
- 不要把 `magpie-marvis-0.2.58-fixed.zip` 当成源码仓库内容上传；它是给你本地备份/解压用的，GitHub 仓库上传目录里的文件即可。
- Android APP 提取的 `marvis-android-uskey` 不在本目录（在 `/sdcard/Download/DSH-Go/marvis-android-uskey`），里面有 `libqimei.so` 和设备指纹，不要上传到公开仓库。

## 上传后

在本机把仓库地址换成你自己的：

```bash
magpie plugin add <你的用户名>/magpie-marvis
```

然后按 `FIX-4100404.md` 配置 `native/` 或 `MARVIS_USKEY_URL`。
