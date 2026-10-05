# Aseprite 构建工作流

[English](README.md)

基于 [a1393323447/aseprite-builder](https://github.com/a1393323447/aseprite-builder) 的分支，通过 GitHub Actions 编译 Aseprite。当前构建矩阵启用 Windows；工作流中也保留了 macOS 和 Linux 的依赖准备与编译分支。

## 构建流程

[工作流文件](.github/workflows/build_and_release.yaml) 获取 Aseprite 上游发布版本，准备 Skia，使用 CMake 生成 Ninja 构建文件，再将可执行程序打包为便携 ZIP。

支持 `workflow_dispatch` 手动触发；`main` 分支的 `BuildLog.md` 发生变更时也会触发构建。

## 使用

1. Fork 仓库并启用 GitHub Actions。
2. 打开 **Actions → Build and release Aseprite**。
3. 点击 **Run workflow**。
4. 查看任务日志及生成的 Release 附件。

实际运行的平台由工作流中的构建矩阵决定。需要构建 macOS 或 Linux 时，应先将对应平台加入矩阵。

## 许可证

本仓库的自动化文件采用 [MIT 许可证](LICENSE)。Aseprite 及其编译产物遵循上游 [Aseprite EULA](https://github.com/aseprite/aseprite/blob/main/EULA.txt)；分享构建产物前应确认相应的分发权限。
