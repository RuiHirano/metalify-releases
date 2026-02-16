# Configure Metalify EA Input Settings

## Strategy Tester Settings
In the Strategy Tester, please configure the following settings.

### Open the Strategy Tester
Select "View" -> "Strategy Tester" from the MT4 upper left menu.

### 1. Select Metalify EA
Select "MetalifyEA.ex4" from the EA selection button.

![AltText {priority}{768x432}](/img/setting_ea.png)

### 2. Select the Currency Pair You Want to Backtest
Select the currency pair you want to backtest from the currency pair selection button.

![AltText {priority}{768x432}](/img/setting_symbol.png)

### 3. Select the Timeframe for the Main Chart
Select the timeframe for the main chart in the Strategy Tester. You can synchronize with charts of other timeframes in the EA input parameters.

If you are trading using fine price movements, we recommend selecting the shortest timeframe among the timeframes you use. For example, if you use 4-hour, 1-hour, and 15-minute charts, select 15-minute as the main chart timeframe.

![AltText {priority}{768x432}](/img/setting_period.png)

### 4. Set the Backtest Period
You can set any period, but we recommend backtesting for a short period such as one week or one month.
If there is no history data for the set period, an error will occur. Please make sure it is within the period of the history data.

![AltText {priority}{768x432}](/img/setting_date.png)

> [!TIP]
> **Recommended: First, try setting a period of the most recent month where history data exists.**

> [!NOTE]
> **If you cannot find the period setting item, the setting item may be hidden at the bottom of the tester**. It will be displayed by expanding the tester screen upward.

### 5. Specify the Spread
We recommend specifying a fixed value for the Spread setting. If you set the Spread to Current, it may result in a large spread when backtesting on weekends, and orders may not be filled.

![AltText {priority}{768x432}](/img/setting_spread.png)

### 6. Turn ON Visual Mode
Visual mode must be turned ON. If it is OFF, an error will occur.

![AltText {priority}{768x432}](/img/setting_visual_mode.png)

> [!NOTE]
> **If you cannot find the visual mode setting item, the setting item may be hidden in the tester display area**. Try scrolling the display area or expanding the screen.

### 7. Set Playback Speed to Maximum
Since you can adjust the speed and play/pause from the Metalify control panel, we recommend setting the tester playback speed to maximum.

![AltText {priority}{768x432}](/img/setting_speed.png)

### 8. Turn OFF Optimization Mode
Optimization mode must be turned OFF. If it is ON, an error will occur.

![AltText {priority}{768x432}](/img/setting_optimization.png)


### Caution

> [!CAUTION]
> In the Strategy Tester settings, the EA may not work if the following items are not set correctly. Please check again before execution.
> 1. **Visual mode is ON**
> 2. **Optimization mode is OFF**
> 3. **Period is set**


Once you have configured the Strategy Tester settings, next let's configure the settings to display charts for multiple timeframes. You can view this from [**Display Multiple Charts**](/docs/offline-chart-settings).
