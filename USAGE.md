# 使用说明

## 适用任务

三个校区对“已开课后退费”采用不同起算日，需要识别并统一。

## 准备输入

课包清单、公开价格、合同摘要、系统收费字段、优惠与赠课规则、退费制度、销售话术、审批流程。使用前先脱敏姓名、联系方式和与任务无关的敏感信息。

## 操作步骤

1. 建立课包唯一编码
2. 抽取各渠道规则
3. 按情景比对
4. 标记冲突与不可执行条款
5. 设计复核用例
6. 输出统一规则和培训要点

## 校验命令

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 状态使用

- `completed`：核心成果完整。
- `completed_with_limits`：只完成可验证部分，并说明受阻范围。
- `needs_input`：缺少关键输入。
- `needs_confirmation`：资料冲突或需人工确认。
- `failed`：工具或计算失败，提供恢复动作。

## 人工确认

财务负责人与法律/合规人员复核收费、赠课、有效期、退费规则和对外口径的最终统一后，成果才可进入正式业务使用。
