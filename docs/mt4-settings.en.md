# Configure MT4 Settings

To integrate the Metalify app with MetaTrader4 (MT4), some settings are required. This guide explains these setting procedures step by step in detail.

## Download MetaTrader4 (MT4)

> [!CAUTION]
> Currently, when you download from [**MetaQuotes official website**](https://www.metatrader4.com/ja/download), **MetaTrader5 is downloaded** instead. The Metalify app does not work with MetaTrader5, so please be careful.
>
> To download MetaTrader4, we recommend **downloading from the official website of brokers such as XMTrading or OandaJapan**.

## 1. Allow DLL Usage from MT4 Tools, Options

1. Launch MT4.
2. Click "Tools" at the top of the menu bar and select "Options" from the dropdown.
3. The Options window will appear, click the "Expert Advisors" tab.
4. Check the "Allow DLL imports" checkbox.
5. Click "OK" to save the settings.

![AltText {priority}{768x432}](/img/allow_dll.png)

## 2. Get the MT4 Data Folder Path

1. Click "File" at the top of the MT4 menu bar.
2. Select "Open Data Folder" from the dropdown menu.
3. The data folder will open in Explorer, so copy and note the path from the address bar.

![AltText {priority}{768x432}](/img/data_folder_path_copy.png)

> [!NOTE]
> If the address bar doesn't enter copy mode, click the blank space on the right side of the address bar.

> [!TIP]
> You can copy by right-clicking the area you want to copy and selecting "Copy" (or pressing Ctrl+C).

## 3. Open Metalify App Settings and Enter the Noted Path

1. Launch the Metalify app.
2. Click the settings icon in the upper right of the header to open the settings section.
3. Paste the path you noted earlier into the MT4 data folder path input field.
4. If the correct path is entered, a checkmark will appear. If incorrect, an error message will be displayed, so check the path again.

![AltText {priority}{768x432}](/img/app_settings.en.png)

> [!TIP]
> After focusing on the area where you want to paste, you can paste by "right-clicking and selecting paste (or pressing Ctrl+V)".

## 4. Click "Install EA" from Metalify App Settings to Install the EA in MT4

1. Click the "Install EA" button in the Metalify app.
2. When installation is complete, a confirmation message will be displayed.

## 5. Restart MT4

1. Close MT4 once.
2. Launch MT4 again.

## 6. Open Strategy Tester, Specify MetalifyEA.ex4, and Run the Backtest

1. Open the "Strategy Tester" panel at the bottom of MT4.
2. Select "MetalifyEA.ex4" from the "Expert Advisor" dropdown.
3. Configure the necessary settings and click the button to start the backtest.

For EA input parameters, please refer to [**EA Input Settings**](/docs/ea-parameters).

![AltText {priority}{768x432}](/img/mt4_backtest.png)

---

This completes the integration settings between the Metalify app and MT4. Use the Metalify app's control panel to efficiently perform operations such as chart progression, placing orders, and making changes during backtesting.
