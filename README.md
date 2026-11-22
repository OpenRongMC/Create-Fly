# Create Fly（RongMC 构建）

基于 Zurrtum 等社区的 **Create** Fabric 移植线，在 RongMC 建筑服使用的 **Minecraft 26.3** 构建（发布文件名 `rongmc-create-fly-*.jar`）。

Create 是大型科技/动力传输模组：传动、加工、物流、列车等。详细玩法请参阅上游 Create 文档与社区教程。

## 重要限制（请先读）

- **本仓库没有可维护的完整 Create 源码树**（本地仅有已构建 jar）。因此 Git 内只有说明与许可证；二进制见 Releases。
- Fabric id **必须保持** `create`：`Create.class` 字节码写死 `getModContainer("create")`，强行改 id 会直接崩溃。
- 仅 jar 文件名使用 `rongmc-` 前缀以区分发行渠道。

## 与常见原版 Create 发行的差异 / 注意

- 版本线为 Fly/Zurrtum 26.3 适配构建（`6.0.9-2` 一带），不是 simibubi 官方 Forge/NeoForge 包。
- 与官方 Create 模组包、其它分支（如 Create Fabric 官方移植）**不要混装**。
- Ponder 教程在部分场景会崩；请同时安装 [Create-Fly-Ponder-Fix](https://github.com/OpenRongMC/Create-Fly-Ponder-Fix)。

## 已知问题

- Ponder：sided filter `orElseThrow`、Deployer 空 OwnerName、方块实体备份等（由 Ponder Fix 缓解，无法保证 100% 教程可点）。
- 大型传动网络在低配设备上 TPS/FPS 压力大（上游通病）。
- 无源码仓无法接受“改 Create 本体”的 PR；请对 Fix 模组或配置侧提需求。

## 许可

本仓文档与发行包装以 **GPL-3.0** 提供（见 `LICENSE`）。Create 上游本身另有许可证，使用二进制时请同时遵守上游条款。
