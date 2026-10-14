# 维护与发布说明

当前包含 8 篇用于展示填表效果的 sample 论文，来源及字段修订见 [Sample Sources](docs/sample-sources.md)。尚未填写数据集或评测条目，不代表完整综述文献库。

<a id="inclusion-criteria"></a>
## 收录标准

- 收录与遥感图像生成相关、具有研究价值的期刊论文及领域认可的优质会议论文。
- 不收录一般低质量 EI 会议论文。会议质量由维护者结合领域认可度和研究贡献审核，不能仅凭 EI 检索决定收录或排除。
- 相关 arXiv 预印本可以收录，Venue 标注为 `arXiv`，并提供具体预印本链接；未经确认，不填写会议录用或期刊发表信息。
- 恢复与重建保留为正常分类，不再标注为可选范围。

## 填写内容

- 在 README 的对应表格中添加条目，按年份从新到旧排序。
- 论文名称链接到论文原始页面；Code、Download 链接到官方代码或数据来源。
- 未公开或未核验的信息保持为空，不使用猜测的会议、年份、作者或链接。
- `More` 列可在发布后链接到本仓库的条目 Issue。
- 分类是暂定目录；确定综述范围后，可删除不适用的空分类，同时更新目录导航。
- 顶部横幅、综述总览图、更新记录、引用与联系方式均已留出位置。图片准备好后再添加本地资源目录。

## 接收投稿

`.github/ISSUE_TEMPLATE/` 提供论文和数据集投稿模板。发布到 GitHub 后可从 New issue 页面使用。

维护者可创建以下标签，再根据条目分配；模板不依赖任何预设标签：

- 类型：`paper`、`dataset`、`benchmark`、`survey`
- 任务：`text-to-image`、`layout-conditioned`、`reference-guided`、`data-synthesis`、`cross-modal`、`restoration`、`other-tasks`
- 状态：`needs-verification`、`verified`

Issue 记录与 README 表格需要人工维护，工作流不会自动收录文献或修改 README。

## 发布前配置

1. 确定 GitHub 仓库的归属和名称，将本目录作为独立仓库上传；不需要上传父目录中的调研文件。
2. 添加真实的维护者信息、简介和收录范围；有对应成果后再添加引用信息。
3. 在 GitHub 创建需要的标签，按真实仓库地址填写 README 的 Issue 导航和统计徽章。
4. 保留 LICENSE 中的上游版权声明与 README 中的来源说明。

## Issue 统计工作流

`.github/workflows/issueStat.yaml` 沿用参考仓库的统计机制，调用第三方 `madderscientist/issueStat` 可复用工作流。入口固定到一个提交版本，其内部依赖仍由第三方工作流管理。

- 在 Issue 打开、关闭、重新打开及标签变更时运行，也支持手动运行。
- 需要读取 Issues、写入仓库内容的权限，通过 GitHub 自带的 `GITHUB_TOKEN` 执行，不需要另填个人令牌。
- 将统计结果写入并更新 `dashboard` 标签；不修改 README，也不生成网站。
- 发布后首次使用前，请确认仓库允许 GitHub Actions 执行。若不需要统计，可删除该工作流。

本地仅提供配置文件；远端运行效果需要仓库发布后通过 GitHub Actions 验证。
