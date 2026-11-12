# 跨项目第三方媒体低成本处理策略

核查日期：2026-11-12

POLICY_STATUS=PROPOSED

RESEARCH_ONLY=YES

## 一、目标

统一管理未授权第三方图片，降低长期维护成本。

## 二、默认处理规则

### VERIFIED：已核实商业使用权限

符合许可证条件时，正常展示图片并保留署名与来源。

### UNCLEAR / UNKNOWN：图片复用权限不明确

不复制、重新托管、嵌入或热链接原图。

默认使用简短文字占位，并按以下顺序选择链接：

1. 可合法公开访问且稳定的原始图片文件 URL。
2. 能直接定位该图片的独立作品详情页 URL。
3. 无上述链接时，仅保留文字说明，不提供误导性链接。

不得使用教材首页、网站首页或搜索结果页
冒充原图链接。

不得抓取受保护图片文件地址、
绕过访问控制或自动生成缩略图。

仅从可靠来源核实精确链接；
不能从作者名称猜测图片 URL。

不要求为每张图片人工搜索链接。
查找成本明显过高时，允许退回文字占位。

### DECORATIVE：装饰性图片

直接省略。

### ESSENTIAL：知识理解必需的地图或图表

省略会影响理解时，保留人工复核标记。
优先选择文字解释或合法的自主生成内容。
不默认购买授权。

## 三、最小通用信息

- media_role
- rights_status
- display_mode
- title
- exact_media_url（可为空）
- exact_asset_page_url（可为空）
- attribution（可为空）
- license_reference（可为空）

display_mode：

LICENSED_IMAGE
EXACT_MEDIA_LINK
EXACT_ASSET_PAGE_LINK
TEXT_NOTE
OMIT
HOLD_REVIEW

不为此创建公共代码库或复杂媒体系统。

## 四、适用边界

不修改 go-dev，不启动批量图片处理或正式开发。
所有项目均不默认购买第三方图片许可。
缺失原图不等于允许复制原图。

## 五、决策

RESULT=PASS

RECOMMENDATION=TEXT_FALLBACK_WITH_EXACT_MEDIA_LINK

IMPLEMENTATION=NOT_AUTHORIZED

RESEARCH_ONLY=YES
