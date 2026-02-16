# FAQ - Frequently Asked Questions

## Table of Contents

---

## 1. About EA

---

### I can't find the "Period" field in the Strategy Tester settings

If you can't find the period setting item, the setting item may be hidden at the bottom of the tester. It will be displayed by expanding the tester screen upward.

### "-MTLF" offline charts are not being generated

If "-MTLF" offline charts are not being generated, the following causes are possible:

- The synchronized chart setting is not set to true in the settings screen
  - Please check if the chart settings are correct in the expert settings screen.
- The EA has terminated due to some error
  - Check the error message from the "Journal" tab in the Strategy Tester, and if an error has occurred, resolve the error.

For specific troubleshooting, please refer to ["**Offline Chart Not Generating**"](/docs/ts-1-offline-chart-not-generate).

If it still doesn't resolve, please contact us from the [Contact](/support/contact) page.

---

### Offline charts are generated but the period differs from the backtest

The offline chart period is generated from the history data of the symbol and period of the generated offline chart (if it's USDJPY-MTLF,H1, it's generated from the USDJPY,H1 history data). Therefore, if the period of the relevant history data differs from the backtest period, the offline chart period may also differ.
If history data for the relevant period is insufficient, downloading history data from "Tools" -> "History Center" may resolve the issue.

---

### The EA terminates immediately

If the EA terminates immediately, please take the following actions:

- The EA has terminated due to some error
  - Check the error message from the "Journal" tab in the Strategy Tester, and if an error has occurred, resolve the error.
- You are specifying a period where data does not exist
  - If the backtest period specifies a period that does not exist in the history data, the EA may terminate immediately. Change the backtest period to a period that exists in the history data.
- Settings are incorrect
  - If settings such as optimization mode being on or visual mode being off are incorrect, the EA may terminate immediately. Check the settings and change them to the correct settings.

For specific troubleshooting, please refer to ["**Tester Stops Immediately After Starting**"](/docs/ts-2-tester-not-start).

---

### Error code 138 occurs and I cannot place orders

Error code 138 indicates that the slippage when placing an order is too large. Increasing the slippage value in the EA settings screen may resolve the issue.

> [!CAUTION]
> If you are running the EA on a holiday, the spread may become large on holidays. In that case, **changing the spread value in the Strategy Tester to a fixed value** may resolve the issue.

---

### I can't find the visual mode and period setting items

If you can't find the visual mode and period setting items, the setting items may be hidden in the tester display area. Try scrolling the display area or expanding the screen.

---

## 2. About Control Panel

---

### User authentication fails

If user authentication fails, please check the following items:

- Is the email address and password correct?
- Is the plan active?
  - Please check from "Subscription" on the Metalify website whether the plan is active.

---

### The connection mark on the control panel does not turn on

The control panel connection mark turns on when the EA is running without errors. If the EA is not running or has terminated due to an error, the connection mark may not turn on. Check the error message from the "Journal" tab in the Strategy Tester, and if an error has occurred, resolve the error.

---

### A security warning is displayed when installing the control app

Currently, due to Windows security settings, a security warning may be displayed when installing the control app. If a security warning is displayed, click the "More info" button and continue with the installation.

---

## 3. About Billing

---

### When is the billing validity period?

The billing validity period is one month from the plan purchase date or plan renewal date. When one month has passed from the plan purchase/renewal date, the plan will automatically be renewed for one month.

---

### If I cancel the plan, will I immediately lose access?

If you cancel the plan, you can continue to use it until the plan validity period ends. When the plan validity period ends, use of the plan will be stopped.

---

## 4. Other Questions

---

### MetaTrader5 was downloaded when I tried to download MetaTrader4

Currently, when you download from the [**MetaQuotes official website**](https://www.metatrader4.com/ja/download), **MetaTrader5 is downloaded** instead. The Metalify app does not work with MetaTrader5, so please be careful.
To download MetaTrader4, we recommend **downloading from the official website of brokers such as XMTrading or OandaJapan**.

---

### What is ForeXpert?

ForeXpert is an app that allows FX automated trading on smartphones. ForeXpert is a separate app from Metalify, but they have the same development and management company. For details about ForeXpert, please check [here](https://forexpert.metalify-fx.com).

---

### Can I use my own MT4 indicators with the Metalify app?

With the Metalify app, you can use your own MT4 indicators. By running the EA in the tester and adding indicators to the displayed chart, you can use your own MT4 indicators.

---

> [!TIP]
> If you have any other questions, please feel free to contact us from the [Contact](/support/contact) page.
