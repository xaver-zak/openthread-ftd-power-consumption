# Power Consumption Analysis of IEEE 802.15.4 Nodes

This repository contains the dataset and processed data for the academic paper **Power Consumption Analysis of IEEE 802.15.4 Nodes**.

The measurements cover the ESP32-H2, nRF52840 and nRF5340 while operating as routers in an OpenThread network. The paper focuses on determining the current consumption of these MCUs in different radio states, primarily during the transmission interval at different TX power settings. Five UDP messages with a 122&#8239;B MAC frame size were sent periodically to establish the mean current draw during transmission for each TX power setting.

All current measurements were recorded with a Keysight N6705A DC Power Analyzer.

## Repository structure

```
power_measurements/
└── keysight n6705a/
    ├── README.md     processed data tables for each MCU
    ├── esp_32/       ESP32-H2
    ├── nrf_52840/    nRF52840 Dongle
    └── nrf_5340/     nRF5340 DK
```

Each MCU folder contains:

- **Raw data** in `.csv` and `.dlog` format, as exported from the Keysight N6705A.
- **Processed data** (`processed_data_*.csv`) with the mean, standard deviation, minimum and maximum current and the mean power during the transmission interval for each TX power setting.

The processed data tables for all three MCUs are in the [measurements README](power_measurements/keysight%20n6705a/README.md).

## License

This dataset is licensed under [CC BY-SA 4.0](LICENSE).
