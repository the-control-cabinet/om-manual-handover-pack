# 05 System index: where each system is documented

[← Back to README](../README.md)

The house is treated as one building with its own services. Each system has a record here (asset register, maintenance, safety) and, where it exists, a repo with the full design and as-built detail.

| System | What it covers | Detailed record |
|---|---|---|
| Heating, DHW and controls | Boiler, cylinders, zone valves, Evohome, junction box | [Evohome](https://github.com/the-control-cabinet/evohome-heating-controls-ramses-integration) · [Plant monitoring](https://github.com/the-control-cabinet/heating-plant-monitoring-esphome) · [Sequence of operation](https://github.com/the-control-cabinet/heating-sequence-of-operation) · [FDD rules](https://github.com/the-control-cabinet/fdd-rules-heating-plant) |
| Cooling and air quality | Aircon, purifiers, humidifier, IAQ sensors | [IAQ monitoring](https://github.com/the-control-cabinet/indoor-air-quality-monitoring) · [Aircon data-point map](https://github.com/the-control-cabinet/localtuya-portable-aircon-dp-map) |
| Electrical | Consumer unit, circuits, RCBOs | This pack (asset register; circuit chart to complete) |
| Fire and CO | Interlinked alarms and their HA interface | [Aico interface](https://github.com/the-control-cabinet/aico-ei413-shelly-ha) |
| Security and access | Intruder alarm, lock, garage, cameras | [Security baseline](https://github.com/the-control-cabinet/smart-home-security-baseline) (details withheld by policy) |
| Water | Stopcock, mains metering and pressure, leak detection | [Mains water metering](https://github.com/the-control-cabinet/mains-water-metering-modbus-rtu) · [Leak detection](https://github.com/the-control-cabinet/layered-leak-detection) |
| Energy | Meters, tariff, EV charging | [Energy dashboard](https://github.com/the-control-cabinet/home-energy-dashboard) · [Demand-side management](https://github.com/the-control-cabinet/demand-side-energy-management) |
| Lighting and shading | Lights, blinds | [Lighting and shading](https://github.com/the-control-cabinet/lighting-and-shading-control) |
| Presence | BLE proxies, room presence | [BLE presence network](https://github.com/the-control-cabinet/esp32-ble-presence-network) |
| Head end and networks | HA host, Zigbee, ESPHome, MQTT, router, backups | [Integration schedule](https://github.com/the-control-cabinet/home-assistant-integration-schedule) · [Zigbee migration](https://github.com/the-control-cabinet/zigbee-network-migration-z2m) · [ESPHome fleet](https://github.com/the-control-cabinet/esphome-fleet-standards) · [Head-end health](https://github.com/the-control-cabinet/head-end-health-monitoring) |
| Occupant interface | Areas, dashboards, automations, notifications | [HA areas, dashboards and automations](https://github.com/the-control-cabinet/ha-areas-dashboards-automations) |
| Alarms and trends | Priorities, alarm register, trend policy | [Alarm and trend strategy](https://github.com/the-control-cabinet/alarm-and-trend-strategy) |
