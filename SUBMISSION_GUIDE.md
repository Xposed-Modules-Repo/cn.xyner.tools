# 提交流程与模板（Xposed Modules Repo）

参考官方说明仓库：`https://github.com/Xposed-Modules-Repo/submission`

## 1. 提交 Issue 创建模块仓库
- 打开仓库 Issues，新建 Issue：
  - Title：`[submission] cn.xyner.tools`
  - 内容可简述模块用途与主页链接
- 机器人会自动创建模块仓库并邀请为管理员。

## 2. 仓库基础信息（Repo Settings）
- Title：`cn.xyner.tools`（包名）
- Description：`Xyner`（模块名）
- Collaborators：模块作者
- Home Page：支持/主页链接（若无可暂留空或指向项目主页）

## 3. 文件与内容
- `SUMMARY`：简要摘要（已在本目录准备）
- `README.md`：完整描述（已在本目录准备）
- `.github/ISSUE_TEMPLATE/`：Issue 模板目录（已创建）
  - `bug_report.md`：Bug 报告模板
  - `feature_request.md`：功能建议模板
  - `question.md`：使用问题模板
  - `config.yml`：模板配置文件

> 备注：官方还支持更多 meta 文件，请按需要参考示例仓库添加。

## 4. Release 发布规范
- Release Title：版本名（例如：`25.1030.1613`）
- Release Content：变更日志
- Release Tag：`[versionCode]-[versionName]`（例如：`303-25.1030.1613`）
- 附件：APK 构建产物（示例现有文件：`app/release/Xyner_25.1030.1613(303).apk`）

## 5. 反馈提交与 Issues 管理

### 反馈渠道
- GitHub Issues：用于 Bug 报告、功能建议、使用问题等
- 在模块仓库中创建 Issue，便于跟踪与回复
- 使用预定义的 Issue 模板（`.github/ISSUE_TEMPLATE/`）可确保包含必要信息

### 反馈内容要求
提交反馈时，请务必包含以下信息：
- **目标应用版本**：受影响的应用名称及版本号
- **系统版本**：Android 系统版本（例如：Android 13）
- **设备信息**：设备型号、制造商等
- **模块版本**：Xyner 模块版本号
- **复现步骤**：详细的操作步骤，便于重现问题
- **日志要点**：相关错误日志或异常信息（如有）
- **问题描述**：清晰描述问题现象或建议内容

### Issues 标签建议
- `bug`：Bug 报告
- `enhancement`：功能建议
- `question`：使用问题
- `compatibility`：兼容性问题
- `documentation`：文档相关

### 反馈处理流程
1. 接收反馈后，根据类型进行分类和标签
2. 复现问题或评估建议的可行性
3. 在相关 Issue 中回复并标记状态
4. 修复后关闭 Issue 并关联到对应的 Release

## 6. 校验清单（Checklist）
- [x] 包名：`cn.xyner.tools`
- [x] Xposed 入口：`assets/xposed_init` -> `cn.xyner.tools.Run`
- [x] minSdk：27（Android 8.1+）
- [x] Xposed API：82（compileOnly）
- [x] 已准备 SUMMARY / README.md
- [x] 已建立反馈渠道与 Issues 管理规范
