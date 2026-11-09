# 输入输出契约

## 输入字段

| 键 | 名称 | 类型 | 必填 |
|---|---|---|---|
| `course_packages` | 课包清单及价格 | array | 是 |
| `contract_rule_summary` | 合同规则摘要 | string | 是 |
| `published_price_list` | 对外价目表 | array | 是 |
| `sales_scripts` | 销售话术 | array | 是 |
| `refund_policy` | 退费制度 | string | 是 |
| `approval_process` | 审批流程 | string | 否 |

## 状态

- `completed`：核心成果完整，关键结论人工确认要求满足。
- `completed_with_limits`：至少一项实质成果，说明限制、已完成和受阻范围。
- `needs_input`：必填字段缺失。
- `needs_confirmation`：资料冲突或人工确认未完成。
- `failed`：计算或工具失败。

## 输出

- `规则一致性矩阵`：结构化条目数组，不允许空壳或占位文本。
- `冲突清单`：结构化条目数组，不允许空壳或占位文本。
- `建议统一口径`：结构化条目数组，不允许空壳或占位文本。
- `情景测试用例`：结构化条目数组，不允许空壳或占位文本。
- `客服/顾问告知模板`：结构化条目数组，不允许空壳或占位文本。

完整机器契约见`contract/input.schema.json`、`contract/output.schema.json`和`contract/runtime_contract.json`。
