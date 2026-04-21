# SilverGarden

## 项目简介 / Introduction
SilverGarden 是一款为 Stellaris（群星）设计的模组，用于实现作者在游玩过程中的一些(yi)小(xiang)巧(tian)思(kai)

## 主要功能 / Features
- 新增领导者特质及其特殊机制
- 领导者相关的专属事件与效果
- 自定义领导者创建、赋能与成长机制

## 未来内容 / TODO
- 总结DMCA相关内容制作特色民政/事件

## 结构优化测试分支 / Refactor Test Branch
- 分支名: `test/refactor-assimilation-structure`
- 目标: 在不改变现有数值与玩法结果的前提下，优化同化流程脚本结构，便于后续维护与平衡调整。
- 本次重构点:
	- 将同化强化逻辑从 `events` 抽离到 `common/scripted_effects`。
	- 将同化后的即时补位与同步逻辑抽离为独立效果。
	- 保持现有经验分档与职业分支的强度表现不变。

## 游玩对比建议 / Playtest Comparison
- 对比分支: `master` vs `test/refactor-assimilation-structure`
- 推荐观察项:
	- 同化后人偶成长幅度是否一致
	- 同化后岗位补位速度是否一致
	- 事件触发稳定性与日志报错情况

## 目录结构 / Directory Structure
```
SilverGarden/
├── common/
│   ├── traits/                # 领导者特质定义 (Leader traits)
│   ├── scripted_effects/      # 领导者相关脚本效果 (Scripted effects)
│   ├── on_actions/            # 游戏事件触发器 (On-action triggers)
│   ...
├── events/                   # 领导者专属事件 (Leader events)
├── gfx/                      # 美术资源 (Graphics)
├── localisation/
│   └── simp_chinese/         # 简体中文本地化 (Simplified Chinese localisation)
├── descriptor.mod            # 模组描述文件 (Mod descriptor)
├── thumbnail.png             # 缩略图 (Thumbnail)
```

## 兼容性 / Compatibility
- 支持 Stellaris 4.* 版本（目前游戏更新均未对mod涉及代码相关进行更改）
- 主要影响领导者、事件与特质系统

## 鸣谢 / Credits
- stellaris及其创作团队
- 灵感与部分文本来源于社区与官方内容

