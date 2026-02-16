# Tester Stops Immediately After Starting

If the tester stops immediately after starting, an error may be displayed. Please identify and resolve the error cause following the steps below.

## 1. Check Settings
Please check whether the Strategy Tester and Expert settings are configured correctly, referring to the following documents.

- [Strategy Tester Settings](/docs/ea-parameters)
- [Display Multiple Charts](/docs/offline-chart-settings)

> [!CAUTION]
> In the Strategy Tester settings, the EA may not work if the following items are not set correctly. Please check again before execution.
> 1. **Visual mode is ON**
> 2. **Optimization mode is OFF**
> 3. **Period is set**
>
> An error will occur if you specify a period where data does not exist. We recommend conducting backtests for a recent period.


## 2. Check Event Log and Operation History
2. Please check the error message from the event log and operation history.

### If the error "no history data 'Currency Pair Name'" is displayed
If an error message like the following is displayed in the operation history, there may be no history data for the relevant period. Please check if the history file for the relevant period exists.

~~~none
🛑 TestGenerator: no history data 'EURJPY-15' from 2024.05.01 to 2024.06.01
~~~

> [!TIP]
> If this error occurs, the event log should also display "Failed to generate offline chart."

### If the error "Reader handle failed" is displayed
If an error message like the following is displayed in the operation history, there may have been a failure in reading the history data. This error has various causes and is difficult to diagnose, so please contact us from the [Contact](/support/contact) page.

~~~none
🛑 [Error:87:0] History file read error.
🛑 [Error:123:0] Reader handle failed.
~~~

> [!TIP]
> If this error occurs, the event log should also display "Failed to generate offline chart."


## 3. If Still Not Resolved
If the issue is not resolved after checking the above steps, please contact us from the [Contact](/support/contact) page. While we cannot promise to resolve all issues, we will provide support to the best of our ability.

> [!NOTE]
> When contacting us, providing the following information will help us respond more smoothly:
> - Screenshot of the tester settings screen
> - Screenshot of the expert settings screen
> - Event log screen at the top of the Metalify control panel
> - Screenshot of the "Journal" tab at the bottom of the tester
>
> (Screenshots taken with a smartphone are fine.)
