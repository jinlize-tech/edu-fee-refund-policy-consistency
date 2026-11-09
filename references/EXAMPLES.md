# 收费与退费规则一致性检查示例

## 典型场景

三个校区对“已开课后退费”采用不同起算日，需要识别并统一。

## 具体示例

输入三个校区规则后，系统以同一张表展示起算日、扣费方式、赠课处理和审批权限差异。

## 脱敏输入示例

```json
{
  "contract_version": "1.2.0",
  "data_status": "confirmed",
  "contains_sensitive_data": false,
  "requested_output_language": "zh-CN",
  "course_packages": [
    {}
  ],
  "contract_rule_summary": "合同规则摘要已核对（脱敏示例）",
  "published_price_list": [
    {}
  ],
  "sales_scripts": [
    {}
  ],
  "refund_policy": "退费制度已核对（脱敏示例）",
  "approval_process": "审批流程已核对（脱敏示例）"
}
```

## 预期处理

1. 运行输入契约校验。
2. 逐项核对输入来源、版本和口径。
3. 按`references/PROFESSIONAL_PLAYBOOK.md`完成专业分析。
4. 输出规则一致性矩阵、冲突清单、建议统一口径等核心成果。
5. 由财务负责人与法律/合规人员确认收费、赠课、有效期、退费规则和对外口径的最终统一后才可作为正式业务结论。

## 不应出现的输出

- 虚构政策、价格、人员、课程或客户事实。
- 以“暂无”“待完善”等占位文本冒充完成。
- 无依据的确定性判断或伪造人工签批。
