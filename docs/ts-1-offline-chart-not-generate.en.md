# Offline Chart Not Displaying

The phenomenon of offline charts not being generated has different causes depending on the inquiries received. Please follow the steps below to identify the cause.

## 1. Check Settings
Please check whether the Strategy Tester and Expert settings are configured correctly, referring to the following documents.

- [Strategy Tester Settings](/docs/ea-parameters)
- [Display Multiple Charts](/docs/offline-chart-settings)

## 2. Check Event Log
Please check the error message from the event log.

If the error is "Offline chart data is insufficient", there may be insufficient data to generate the offline chart. Proceed to step 4 to check if the history file for the relevant period exists.

![AltText {priority}{768x432}](/img/eventlog-error-offline-history-insufficient.png)

## 3. Check Operation History



### If the error "no history data 'Currency Pair Name'" is displayed
If an error message like the following is displayed in the operation history, there may be no history data for the main chart timeframe set in the Strategy Tester. Proceed to step 4 to check if the history file for the relevant period exists.

~~~none
🛑 TestGenerator: no history data 'EURJPY-15' from 2024.05.01 to 2024.06.01
~~~

> [!TIP]
> If this error occurs, the event log should also display "Failed to generate offline chart."


### If No Error is Displayed
If no error is displayed and "Offline chart generated" is shown in the event log, there may be an expert settings configuration error or an oversight of offline chart files. Please check the following steps.
- Check whether the offline chart flag is set to true in the expert settings.
- Start the tester again and check whether the "MTLF" file is generated in the offline chart list screen.

## 4. How to Check History Files for the Relevant Period

Click "Offline Chart" from "File" in the menu bar at the top of MT4.

Check whether history data exists for the relevant currency pair and period.

![AltText {priority}{768x432}](/img/offline_chart_no_history_data.png)


> [!TIP]
> In the above image, if you run the tester with "USDJPY,D1" where data does not exist, or "USDJPY,H1, 2022.01.01 ~ 2022.02.01" where the period is insufficient, offline charts will not be generated and an error will occur.


If history data does not exist, downloading history data may resolve the issue. For details, please refer to "[Download Historical Data](/docs/download-history-data)".


## 5. If Still Not Resolved
If the issue is not resolved after checking the above steps, please contact us from the [Contact](/support/contact) page. While we cannot promise to resolve all issues, we will provide support to the best of our ability.

> [!NOTE]
> When contacting us, providing the following information will help us respond more smoothly:
> - Screenshot of the tester settings screen
> - Screenshot of the expert settings screen
> - Screenshot of the offline chart list screen
> - Event log screen at the top of the Metalify control panel
> - Screenshot of the "Journal" tab at the bottom of the tester
>
> (Screenshots taken with a smartphone are fine.)
