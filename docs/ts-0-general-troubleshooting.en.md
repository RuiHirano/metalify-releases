# General Errors and Troubleshooting

This page explains general errors that occur in Metalify. When an error occurs, please refer to the following steps.

# How to Check the Event Log
When an error occurs, the error message is basically displayed in the event log. Check the error message and identify the cause.

## 1. Display the Event Log
When you click the "Event Log" button at the top of the Metalify control panel, the event log will be displayed. Error messages are displayed here.
![AltText {priority}{768x432}](/img/eventlog-error-control-panel.png)

## 2. Check the Event Log Error Message
Check the error message and identify the cause. The response method differs depending on the content of the error message.

![AltText {priority}{768x432}](/img/eventlog-error-eventlog-screen.png)

## 3. Check Error Message Details
When you click the "Details" button on the right side of the error message, you can check the details of the error message. Check the details and identify the response method.
![AltText {priority}{768x432}](/img/eventlog-error-detail.png)



# Error Messages and Response Methods
The following introduces general error messages and their response methods.

## EA is not running in visual mode
This error message is displayed when the Expert Advisor (EA) is not running in visual mode. Please turn on visual mode with the following steps.

1. Open the Strategy Tester settings screen
2. If visual mode is OFF, switch it to ON
3. Run the test again

![AltText {priority}{768x432}](/img/eventlog-error-eventlog-screen.png)



## Please disable EA optimization
This error message is displayed when Expert Advisor (EA) optimization is enabled. Please disable optimization with the following steps.

1. Open the Strategy Tester settings screen
2. If optimization mode is ON, switch it to OFF
3. Run the test again

![AltText {priority}{768x432}](/img/eventlog-error-ea-optimization-invalid.png)


## Offline chart timeframes are duplicated
This error message is displayed when the timeframe of the Strategy Tester's main chart and the offline chart timeframe are duplicated. Please correct the timeframe with the following steps.

1. Open the Strategy Tester's expert settings screen
2. Set the flag to false where the timeframe duplicates with the main chart, or change the timeframe
3. Run the test again

![AltText {priority}{768x432}](/img/eventlog-error-period-duplicate.png)

## Offline chart data is insufficient
This error message is displayed when offline chart data is insufficient.

For response methods, please refer to ["Offline Chart Not Generating"](/docs/ts-1-offline-chart-not-generate).

![AltText {priority}{768x432}](/img/eventlog-error-offline-history-insufficient.png)
