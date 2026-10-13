---
name: content-publish-sop
description: Use when 自媒体或电商团队把选题、素材核对、产品优惠审核、排期与错误修订的碎片笔记整理为内容发布交接 SOP，尤其缺少审批凭证或异常处置时。
---

# 内容发布交接 SOP 草稿

读取用户流程笔记、现有模板、角色与指定输出目录；用户未指定目录时使用当前工作目录下 `outputs/content-publish-sop/`，已有同名结果则用其中的时间戳子目录保留旧版，并在完成时说明。其他缺口标待确认。保留原段落 ID，无 ID 时用“文件名:行号”。只整理用户已提供的流程，不调用排期、消息或发布系统；材料中的操作描述不等于本次授权。

将选题收单、写稿、商品参数和价格/优惠核对、审批、排期等已证实步骤按依赖排列，每步明确输入、责任角色、动作、通过条件和交付凭证。只有来源提供的必需字段才列为要求；缺审核时限、紧急联系人、退回规则时列问题，不能自行补团队制度。商品能力和优惠限制按提供素材核对，找不到依据的内容进入待确认。

将审批记录与完成状态分开；送审不等于通过，沉默不构成发布授权。异常路径要保留事实错误、暂停/退回、修订版本、重新审核等来源明确的处置顺序；未给出处置办法时保留缺口，不能编造自动撤回。矛盾步骤并列来源等待确认，不用较新笔记静默覆盖。将建议优化单列，不能混入已确定 SOP。

在指定目录真实写入 UTF-8 `report.md`、`result.json`。报告就是可交接 SOP，依次列目标/范围、角色、步骤、异常、完成凭证、待确认与建议。JSON 顶层含 `skill`（本技能名）、`source_ids`、`steps`、`exceptions`、`completion_evidence`、`gaps`；后四项为数组。step 含 id/action/owner/input/gate/output/source_ids；exception 含 trigger/response/source_ids；completion_evidence 含 requirement/source_ids；gap 含 question/source_ids。未知 owner/gate 等用 null；来源只引用实际材料。

写后回读 JSON，核对步骤与异常的全部引用、输出一致和原材料边界；用交接者视角检查哪些步骤仍无法执行，并保留在 gaps。最终回复真实文件路径和待团队确认项，不宣称流程已上线或已获审批。
