# 更新日志

本文件记录 caiyun-weather skill 的所有重要变更。

## [1.0.0] - 2026-02-27

### 新增

- 基于 [mcp-caiyun-weather](https://github.com/caiyunapp/mcp-caiyun-weather) 创建 OpenClaw Skill
- 支持 5 种天气查询：实时天气、72 小时逐小时预报、7 天一周预报、24 小时历史天气、天气预警
- 支持通过城市名称查询（中文/英文），用户无需提供经纬度
- 内置 46 个中国主要城市坐标，查询即时完成
- 不在内置列表中的城市自动通过 OpenStreetMap Nominatim 在线地理编码
- 保留 `--lng`/`--lat` 参数用于精确坐标查询
- 仅依赖 Python 标准库，无需额外安装
- 实时天气包含空气质量（PM2.5、PM10、O3、SO2、NO2、CO）和 AQI 指数
- 实时天气包含生活指数（紫外线、舒适度）
