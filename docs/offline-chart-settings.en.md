# Display Multiple Charts

By displaying multiple charts, you can obtain more information and improve trading accuracy. With Metalify, you can display up to 4 charts simultaneously.

## EA Input Parameter Settings

### Open the Expert Settings Screen
When you click the "Expert properties" button on the Strategy Tester settings screen, the screen for setting EA input parameters will appear.

![AltText {priority}{768x432}](/img/expert_settings.png)

### Enter the EA Input Parameters

When using Metalify's EA, setting the input parameters is important to get optimal backtest results. The following table lists the EA input parameters. You can synchronize up to 3 charts in one backtest, which means you can view **a total of 4 charts** simultaneously including the main chart.

| Parameter Name | Description | Type | Default Value |
| :---- | :---- | :---- | :---- |
| **Maximum Allowed Slippage** | Maximum allowed slippage when placing orders | Numeric | 20 |
| **Auto Open Offline Charts** | Whether to automatically open offline charts | true/false | true |
| **Offline Chart1 Flag** | Whether to create the first synchronized chart | true/false | false |
| **Offline Chart1 Period** | Period for the first synchronized chart | Period | H1 |
| **Offline Chart2 Flag** | Whether to create the second synchronized chart | true/false | false |
| **Offline Chart2 Period** | Period for the second synchronized chart | Period | H4 |
| **Offline Chart3 Flag** | Whether to create the third synchronized chart | true/false | false |
| **Offline Chart3 Period** | Period for the third synchronized chart | Period | D1 |


> [!CAUTION]
> **Do not specify the same timeframe as the main chart timeframe you are running in the Strategy Tester.**
>
> If you specify the same timeframe, the EA may not work correctly. For example, if you set the main chart timeframe to 1 hour in the Strategy Tester, specify a **timeframe other than 1 hour** for the synchronized chart timeframe.

![AltText {priority}{768x432}](/img/mt4_ea_settings.png)

> [!NOTE]
> In the above image, the following settings are configured:
> - Maximum Allowed Slippage: 20
> - Auto Open Offline Charts: true (Automatically open offline charts)
> - Offline Chart1 Flag: true (Generate the first offline chart)
> - Offline Chart1 Period: 1 Hour (Set the first offline chart timeframe to 1 hour)
> - Offline Chart2 Flag: true (Generate the second offline chart)
> - Offline Chart2 Period: 4 Hours (Set the second offline chart timeframe to 4 hours)
> - Offline Chart3 Flag: true (Generate the third offline chart)
> - Offline Chart3 Period: 1 Day (Set the third offline chart timeframe to daily)

### Open the Offline Chart
If you set the synchronized chart to True, offline chart data with the "-MTLF" suffix will be generated at the start of the backtest (after history data processing).

If the **Auto Open Offline Charts** parameter is set to **true** (default), offline charts will be opened automatically. If you want to open them manually, set this parameter to **false**.

To manually open an offline chart:
1. Click "Start" in the Strategy Tester to begin the backtest.
1. Select "File" -> "Open Offline" from the MT4 menu to display the offline chart list.
2. Open the file with the "-MTLF" suffix attached to the period of the generated offline chart.
3. The offline chart will be displayed and you can confirm that it moves synchronized with the main chart.

> [!TIP]
> If you generated a 1-hour offline chart for USDJPY, the file name will be "**USDJPY-MTLF,H1**".

![AltText {priority}{768x432}](/img/offline_chart_folder.png)

> [!NOTE]
> If the offline chart has not been generated or you are unsure about the setting method, please contact us.

Once you have confirmed the offline chart operation, next we will introduce how to play the backtest and place orders using the Metalify control panel. Please refer to [**Using the Control Panel**](/docs/control-panel).
