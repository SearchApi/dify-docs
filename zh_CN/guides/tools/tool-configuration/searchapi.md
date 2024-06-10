# SearchApi
SearchApi 是一个实时 SERP API，提供来自多种搜索引擎的结构化数据，包括 Google 搜索、Google 购物、Google 工作、YouTube、Amazon 等。

## 1. 获取 SearchApi API 密钥
在 searchapi.io 注册一个免费账户并获取 API 密钥。

## 2. 使用 Google 搜索、Google 新闻、Google 工作或 YouTube 字幕工具
- Google 搜索、Google 新闻、Google 工作：这些引擎需要一个搜索查询。
- YouTube 字幕工具：这个工具需要一个 `video_id`。

SearchAPI 类允许你查询这些工具并处理结果。

### 对于 Google 搜索，结果可以包括：

对于 `result_type=text`:
- `answer_box`（字段：`answer`，`snippet`）
- `knowledge_graph`（字段：`description`）
- `organic_results`（字段：`snippet`，`link`）

对于 `result_type=link`:
- answer_box（字段：`organic_result`，子字段：`title`，`link`）
- organic_results（字段：`title`，`link`）
- related_questions（字段：`title`，`link`）
- related_searches（字段：`title`，`link`）

## 集成新的 SearchApi 引擎
要将新引擎集成到 SearchApi 中，请按照以下步骤操作：

1. 复制现有的工具代码。
2. 修改 `get_params` 请求参数以适应新引擎。
3. 调整 `_process_response` 以处理并返回根据你的需求处理的响应。

按照这些说明，你可以轻松扩展 SearchApi 的功能，包括新的搜索引擎，并自定义数据处理和返回的方式。
