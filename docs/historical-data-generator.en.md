# (Optional) Generate Historical Data

The Historical Data Generator automatically creates MT4 offline chart historical data (HST files) based on Axiory's 1-minute (M1) data.

## Overview

This feature automatically performs the following tasks:

1. Downloads Axiory's M1 historical data from the cloud
2. Aggregates data into specified timeframes (M5, M15, H1, etc.)
3. Generates HST files compatible with MT4 offline charts
4. Places files in MT4's history folder

> [!NOTE]
> Data quality and accuracy depend on Axiory's provided data.

## Prerequisites

Before generating historical data, the following setup is required:

### MT4 Data Folder Configuration

1. Open "Settings" from the menu in the top-right of Metalify Controller
2. Enter your MT4 data folder path in "MT4 Data Folder Settings"
   - You can find this path in MT4: "File" → "Open Data Folder"
   - Example: `C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx`

![AltText {priority}{768x432}](/img/app_settings.en.png)

> [!WARNING]
> If the MT4 data folder is not configured, a warning will appear in the Historical Data Generator dialog, and generation will be disabled.

## How to Use

### 1. Open Historical Data Generator Dialog

Click "Generate Historical Data" from the menu in the top-right of Metalify Controller.

![AltText {priority}{768x432}](/img/historical-data-open-dialog.en.png)

### 2. Select Server Name

Choose or enter your MT4 server name.

- Select from the dropdown list of existing servers
- Manually enter if not in the list
- Examples: `Default`, `FXDD-MT4 Demo Server`, `Axiory-Demo`

![AltText {priority}{768x432}](/img/historical-data-server-select.en.png)

> [!TIP]
> The server name determines where HST files are saved. Make sure it matches the server name used in your MT4.

### 3. Select Symbol (Currency Pair)

Choose a currency pair from the dropdown.

Available symbols:

- **Major pairs**: EURUSD, USDJPY, GBPUSD, USDCHF, etc.
- **Cross pairs**: EURJPY, GBPJPY, AUDJPY, EURGBP, etc.
- **Precious metals**: XAUUSD (Gold), XAGUSD (Silver)

![AltText {priority}{768x432}](/img/historical-data-symbol-select.en.png)

### 4. Set Period

Specify the period for downloading data.

- **From Year**: Select from 2015 to 2025
- **To Year**: Select from 2015 to 2025

Example: For data from 2020 to 2025

- From Year: 2020
- To Year: 2025

![AltText {priority}{768x432}](/img/historical-data-period-select.en.png)

> [!NOTE]
> Longer periods require more time for downloading and generation.

### 5. Select Timeframes to Generate

Check the timeframes you want to generate.

Available timeframes:

- M1 (1 minute)
- M5 (5 minutes)
- M15 (15 minutes)
- M30 (30 minutes)
- H1 (1 hour)
- H4 (4 hours)
- D1 (Daily)
- W1 (Weekly)
- MN1 (Monthly)

Convenient features:

- "Select All": Check all timeframes at once
- "Deselect All": Uncheck all at once

![AltText {priority}{768x432}](/img/historical-data-timeframe-select.en.png)

> [!TIP]
> Select only the timeframes you need for backtesting to reduce generation time.

### 6. Start Generation

Click the "Generate" button to start historical data generation.

A blue progress message will appear during generation.

### 7. Generation Complete

When generation completes, a green success message appears.

- A list of generated HST files is displayed
- Click "Open History Folder" to view the location of generated files

![AltText {priority}{768x432}](/img/historical-data-success.en.png)

## Generated Files

Historical data is saved to the following path:

```
[MT4 Data Folder]/history/[Server Name]/[Symbol]-GEN[Timeframe].hst
```

Example:

- Server Name: `Default`
- Symbol: `EURUSD`
- Timeframes: M5, H1, D1 selected

Generated files:

```
C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx\history\Default\EURUSD-GENM5.hst
C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx\history\Default\EURUSD-GENH1.hst
C:\Users\YourName\AppData\Roaming\MetaQuotes\Terminal\xxxxx\history\Default\EURUSD-GEND1.hst
```

> [!NOTE]
> The `-GEN` suffix is automatically appended to symbol names.

That's it! Historical data generation is complete. You can now use the generated data to run backtests on MT4 offline charts. For detailed backtest instructions, see [How to Backtest](/docs/how-to-backtest).
