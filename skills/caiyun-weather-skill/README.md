# 彩云天气 OpenClaw Skill

一个基于[彩云天气 API](https://docs.caiyunapp.com/weather-api/) 的 [OpenClaw](https://openclaw.ai) Skill，支持查询全球任意城市的实时天气、逐小时预报、一周预报、历史天气和天气预警。

基于开源项目 [mcp-caiyun-weather](https://github.com/caiyunapp/mcp-caiyun-weather) 改造。

## 功能特性

| 功能 | 说明 |
|------|------|
| 实时天气 | 温度、湿度、风速风向、降水、空气质量（PM2.5/PM10/O3 等）、AQI、生活指数 |
| 逐小时预报 | 未来 72 小时逐小时温度、天气、降水概率、风力 |
| 一周预报 | 未来 7 天每日最高/最低温、天气、降水概率 |
| 历史天气 | 过去 24 小时逐小时温度和天气 |
| 天气预警 | 当前生效的气象预警信息 |

## 使用方式

安装后，直接用自然语言向 AI 提问即可：

- "北京现在天气怎么样？"
- "上海明天会下雨吗？"
- "深圳未来一周天气预报"
- "广州空气质量如何？"
- "成都有没有天气预警？"

**用户无需提供经纬度**，只需说出城市名称。

## 安装

将 `caiyuan_weather` 文件夹复制到以下任一位置：

- **工作区级别**（优先级最高）：`<你的项目>/skills/caiyuan_weather/`
- **用户级别**：`~/.openclaw/skills/caiyuan_weather/`

或通过 ClawHub CLI 安装：

```bash
clawhub install caiyun-weather
```

## 前置条件

1. **Python 3**（macOS/Linux 系统自带）
2. **彩云天气 API Token** — 在 https://docs.caiyunapp.com/weather-api/ 免费申请

使用前设置环境变量：

```bash
export CAIYUN_WEATHER_API_TOKEN="你的API密钥"
```

## 内置城市

内置 46 个中国主要城市坐标，查询即时完成，无需网络解析：

北京、上海、广州、深圳、杭州、成都、武汉、南京、重庆、西安、天津、苏州、郑州、长沙、青岛、大连、厦门、昆明、贵阳、哈尔滨、沈阳、长春、福州、合肥、济南、南昌、石家庄、太原、呼和浩特、南宁、海口、三亚、拉萨、乌鲁木齐、兰州、西宁、银川、香港、澳门、台北、珠海、东莞、佛山、无锡、宁波、温州

其他城市（含全球城市）通过 OpenStreetMap 在线地理编码自动解析。

## 技术说明

- 仅使用 Python 标准库，无需 `pip install` 任何依赖
- 彩云天气 API v2.6
- 全球可用，中国地区数据最为精准
- 有频率限制，请避免短时间内重复请求

## 许可证

MIT
