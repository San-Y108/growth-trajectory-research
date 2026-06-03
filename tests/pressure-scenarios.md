# Pressure Scenarios for growth-trajectory-research

RED 阶段 baseline 失败模式（来自 spec 自审分析）：

1. **鸡汤化**：用"他很努力""他有远见"代替证据分析
2. **来源单一**：只用最容易找到的传记摘要或 PR 材料
3. **时间线幻觉**：没有日期支撑就编造成长路径
4. **因果过度声称**：把时间先后当因果关系
5. **幸存者偏差**：只看成功者，忽略同样做法但失败的人
6. **自述当事实**：把本人访谈/自传当客观记录
7. **同名混淆**：不确认身份就开始分析
8. **忽略冲突**：来源有矛盾时选一个版本，不说明
9. **泛化建议**：输出"要努力""要敢于冒险"等无证据绑定的建议
10. **隐私越界**：分析不相关的私人细节

## Scenario 1: PR-heavy Founder

**Prompt**: "告诉我 Elon Musk 是怎么成功的，分析他的关键选择和转折点。"

**Without skill (expected failures)**:
- 接受 Musk 自述和公司叙事作为事实
- 忽略争议、失败、特权背景
- 输出"远见+执行力"式鸡汤
- 不分析 SpaceX/Tesla 早期几乎破产的风险决策

**With skill (expected pass)**:
- 多来源交叉验证关键事件
- 标注哪些是自述、哪些有独立记录
- 分析高风险押注的具体条件和代价
- 包含失败、争议、不可复制因素

## Scenario 2: Conflicting Sources

**Prompt**: "分析 Oprah Winfrey 的成长轨迹，她的早期经历和关键转折。"

**Without skill (expected failures)**:
- 选择一个版本的"逆境翻盘"故事
- 不标注来源冲突
- 把励志叙事当事实

**With skill (expected pass)**:
- 保留来源冲突
- 区分有据事实和本人叙事
- 分析逆境如何可能塑造了具体技能（用置信标签）

## Scenario 3: Common-Name Ambiguity

**Prompt**: "分析 Michael Jordan 的成长轨迹和成功经验。"

**Without skill (expected failures)**:
- 假设是篮球运动员
- 不确认身份就开始分析

**With skill (expected pass)**:
- 识别歧义，简短询问用户确认
- 或说明假设的身份并继续

## Scenario 4: Survivorship Bias

**Prompt**: "成功辍学生有什么共同特质？我能从他们身上学到什么？"

**Without skill (expected failures)**:
- 列出"敢于冒险""不走寻常路"等特质
- 不提基准率（绝大多数辍学生没有成功）
- 把幸存者特征当成功原因

**With skill (expected pass)**:
- 明确标注幸存者偏差
- 提供具体基准率数据（如辍学生整体成功率、收入差距等）
- 说明这些特质在失败辍学生中可能同样存在
- 区分可迁移原则和不可模仿的选择
- 如果找不到具体数据，必须说明这是分析局限

## Scenario 5: Nonlinear Career

**Prompt**: "分析 Vera Wang 从滑冰/新闻到时尚界的成长路径。"

**Without skill (expected failures)**:
- 把转折描述为"命中注定"
- 不分析约束条件、资源、时机
- 输出"追随热情"式建议

**With skill (expected pass)**:
- 分析每次转折的具体约束和替代选项
- 标注哪些是能力积累、哪些是时机运气
- 区分可迁移模式和特定条件

## Scenario 6: Controversial Figure

**Prompt**: "分析 Steve Jobs 的成长轨迹，包括他的好选择和坏选择。"

**Without skill (expected failures)**:
- 英雄崇拜式叙事
- 忽略他的管理问题、被赶出苹果、对家人的态度
- 输出"完美主义+极简"式鸡汤

**With skill (expected pass)**:
- 纳入失败、被解雇、回归
- 分析好选择和坏选择
- 标注哪些值得学习、哪些是代价、哪些不应模仿

## Scenario 7: Adversity-to-Breakthrough

**Prompt**: "告诉我 Howard Schultz 是怎么从贫民窟走出来创办 Starbucks 的。"

**Without skill (expected failures)**:
- 简化为"逆境→奋斗→成功"线性叙事
- 不分析具体的机会、资源、人脉、时机
- 把逆境浪漫化为成功的必要条件

**With skill (expected pass)**:
- 分析具体转折点的条件和替代选项
- 标注哪些是个人努力、哪些是机遇
- 区分可迁移原则和不可复制因素

## Pass/Fail Checklist

每个场景的输出必须通过以下检查：

- [ ] 有来源概览，不是凭空分析
- [ ] 身份已确认或歧义已标注
- [ ] 时间线有日期和置信度
- [ ] 关键判断有来源支撑或标注为推断/合理/推测
- [ ] 来源冲突已保留和说明
- [ ] 纳入了失败、争议、代价、不可复制因素
- [ ] 经历塑造分析使用了置信标签
- [ ] 行动启发绑定证据，不是泛泛建议
- [ ] 有"不应得出的结论"部分
- [ ] 有 2-3 个启发性互动追问
- [ ] 没有鸡汤化、因果过度声称、幸存者偏差
