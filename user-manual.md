

# USER MANUAL

Version 1.5 -- Last update: May 01, 2024
User Role: Broker


##  Login & Register

URL to log in to the application: https://app.beetrade.com

User can login to the application through your email account (created by
admin)

If user registers the new account by himself or selects it via Google
account, the standard price plan is **free** and **normal user role**.
This role can only access **Smart View** and **Terminal** page.

If admin creates a new account with the user\'s email. The user will
receive an invitation email including the credential (email, password)
for logging into the system. The invitation email as the following
screenshot


## List of Features for Broker Users

The following are 6 available features in the Bee platform:

- **Bee Account**: Manage the associated trading accounts, with the
  option to group them by clients

  - Supported brokerages in Bee: Binance, and SSI, DNSE in Vietnam
    Market. To connect to a broker account, users need to provide
    specific authentication details, which vary by brokerage.

- **Bee Terminal/ SmartView**

  - Market Data with Charting Tool & AI Assistant: View and analyze
    market data using an intuitive charting tool, enhanced with AI
    assistance for insights.
  - Integrated Multi-Broker Trading: Seamlessly integrate multiple
    brokerages into a single trading terminal.

- **Bee Order:** A robust tool for creating and managing orders across
  multiple brokers.

  - Supported Basic Orders: Limit, Market, and Advanced orders.
  - Supported Conditional Orders: Bracket, One Cancels Other (OCO), One
    Triggers Other (OTO), One Cancels One Triggers Other (OCO + OTO)
  - Advanced trading tool: Basket, TWAP

- **Bee Algo:** Support user to design trading strategies using an
  intuitive editor and AI assistant

  - Visualize generated trading algorithm in a tree structure, enabling
    easy navigation, understanding and editing
  - Supports a variety of trading indicators and patterns
  - Allow to run Back testing & Live Trading

- **Bee Market Place**

  - Bee users can access shared trading strategies from the community,
    published by users through Bee Algo module. These strategies include
    algorithms data under a tree structure, along with performance
    metrics from their back testing results.
  - Users can view and clone these strategies to edit or further enhance
    them.

- **Bee Portfolio**

  - Bee users can manage total assets and portfolios across all client
    and associated trading accounts.
  - Total assets are aggregated daily to reflect changes, with options
    to filter by specific brokerages and accounts.
  - Portfolio charts display the holdings, including the number of
    stocks, symbols, and their percentage contributions to the user\'s
    overall portfolio in Bee.

## Bee Accounts

These are the associated trading accounts that the user wants to use
with Bee. This configuration is required for new users, as it will be
used for other key features such as Order, Back Test, and Live Trading.

By default, there is a predefined label: [Personal Account.]{.underline}
Additionally, [the user can group trading accounts by clients, but this
is optional.]{.underline}

Currently, Bee supports the trading account from these brokerages:

- **Binance** (Spot
- SSI, DNSE in Vietnam Market. Support both **Cash and Derivative
  Account**

To connect to a broker account, users need provide specific
authentication details, which specify by brokerage.

Click on 'Brokerage Account' from the navigation to access "Account"
page, that user see all the configure trading accounts


### How to add new trading account

To add a new trading account, click on "Add New Account" from the
floating button in the bottom-right corner. A trading account requires
the following information:

- Brokerage: The user needs to specify the trading account and the
  platform it is associated with

- Depending on the selected brokerage, the user must enter the
  authentication information to establish a connection with the broker.
  There are different authentication parameters for each brokerage.

  - Binance: API Key, Secret Key
  - DNSE: Username, Password
  - SSI: Account ID, Consumer ID, Consumer Secret, Private Key

- Click on "Save" to submit. If the authentication information is
  correct and valid, the submission will be successful.

The list of trading accounts will be displayed in this dropdown in the
navigation bar and will be used across multiple features:


### How to add a new client account

In case, user wants to group trading accounts by clients (this step is
optional), clicking on "Add New Client" from the floating button in the
bottom right corner of page to open the following popup

Once a new client account is created, the user can locate the trading
account in the new client profile

## Bee Terminal / SmartView

The main function of this page is to help the user see the market data
from the different sources and take advantage of GPT to analyze the
context from trading view screenshots.

> Note: Please make sure that you have already selected a brokerage
account in the navigation bar. The list of stocks and the watchlist will
be displayed according to the selected brokerage accounts.

### How to create a new conversation in the GPT Assistant

- Choose a symbol in the left panel, user can search or find the stock
  from the watchlist.

  - The selected stock information will be display in the middle panel
    with trading view
  - If selected stock information has GPT Assistant history, the system
    also shows the history chat in GPT Assistant panel.

- In the trading view, click on "GPT Assistant" or click on "Camera"
  icon in chat panel, the application will take a screenshot from the
  current trading view as image.

  - User can ask GPT or use some suggestions question to ask GPT helps
    based on the screenshot context

For each symbol, the application will save the GPT chat as a conversion.
In the future, this conversion data will be used to improve the GPT
response.

A new version of Terminal has been developed, named Smart View. In
addition to analyzing trading view screenshots, the new AI agent
supports querying market data and conducting deep research and reports


## Bee Orders

This feature is used corresponding to a specific trading account. In
order to create an order for the broker, the user needs to make sure
that the selected trading account's connection is valid.

Once user selects a brokerage account, the application displays the
asset of the associated account in the top right corner.


### How to create new order(s)

To create an order, nested orders, or a set of orders, follow these
basic steps:

- Step 1: Select a specific symbol to see the detailed information and
  stock data history in the trading view

- Step 2: Select one of 3 order creation options: Basic Order \|
  Conditional Order \| Advanced Order

  - Currently, the application support 2 order type: Limit & Market
  - The input of an order requires:

    - Symbol name: By default, the symbol is selected symbol that is
      user selected in the first step. User can change it if needed
    - Order Side: Buy or Sell
    - Order type: Limit or Market
    - Quantity
    - Price: Corresponding to the selected broker account, the currency
      will be displayed. If order type is market, the price will be the
      current data market pricing

    - Time in Force:

      - GTD: []{.mark}Good Till Date \| Orders remain in effect until
        the end of the designated day of expiration or until
        specifically canceled or filled.
      - GTC: Good Till Canceled \|Orders remain in effect from
        day-to-day until specifically canceled or filled

- Click on "Submit Order" to complete

### What is the different between Basic \| Conditional \| Advanced Order

- Basic order: For creating a single order. It could be a
  limit order or market order
- Conditional order: For creating combination/ conditional
  order based on 2 types of order (limit, market), including:

  - Bracker Order: help user avoid losses and lock in profits by
    \"bracketing\" an order with two opposing orders, including:

    - Primary order: A BUY order is bracketed by a sell limit order on
      the upside and a sell stop order on the downside.
    - Secondary orders: 2 SELL orders are a buy limit order on the
      upside (take profit order) and a buy limit order on the downside
      (stop loss order)

- One Cancel Other: To create multiple potential orders based on
  specified conditions. Once the first of potential order(primary) is
  filled (including partial filled), the remaining orders are
  immediately to be canceled

- One Trigger Other: is a type of conditional order where the execution
  of a primary order triggers the placement of one or more secondary
  orders.

- One Trigger One Cancel Other: Allow to create a primary order which,
  if executed, triggers the secondary orders. If either of these
  secondary orders is executed, the other is automatically canceled.

- Advanced order: Support user to create multiple orders.

  - [Basket order]{.underline}: Basket orders support user to create a
    single transaction to buy or sell a group (or \"basket\") of
    multiple stocks or other securities simultaneously.

   - TWAP: TWAP order is a trading order strategy that helps
  traders to bull or sell to attain this average price over a set time
  period.

     - TWAP algorithm calculates the average price between the time the
    order is submitted and when it\'s completed. The goal is to keep the
    price close to the true market price


### How to monitor the orders that's triggered from Bee

Once the user submits the order, user can track the status of order in
these panel:

Important Notes:

- All orders that's triggered from Bee are stored and
  displayed in Open Order/ Baset / TWAP Order and History Tab

  - If any orders are triggered but not from Bee, they will be displayed
    here.
- For conditional orders the application will hold the
  secondary orders to wait for the status of the primary order.

- An indicator is to let users know whether the order has been
  successfully submitted to the broker or not. The cancellation icon is
  displayed in each order and is available to trigger a cancellation
  request.

  - If cancellation icon is not displayed, it means that the order is
    held in the application (with conditional order) or that the order
    is invalid to submit to the broker (the application checks the
    validity of the order before submitting it to the broker)

- For an invalid status, the user can view the detailed reason by
  hovering the mouse over the icon in the Note column.

## Bee Algo 

This page allows users to design a trading strategy using custom
parameters and conditions in a tree-view editor with AI. Based on
predefined logic, users can run a back test to evaluate historical
market data, enabling them to make informed predictions about whether to
buy or sell in the future

### Intuitive Tree Editor for Strategy Management

The intuitive tree editor empowers users to seamlessly transition from
strategy creation to real-time execution:

- Strategies Management: The left panel features a list of strategies,
  that user created. Key information, such as symbol and indicators
  used, is conveniently tagged for easy identification.

- Detailed strategy configuration and main actions:

  - Define your trading strategy by setting up logic for buying and
    selling assets using a tree-structured editor based on market
    conditions.
  - Configure parameters to run backtests and evaluate historical market
    data.
  - Trigger live trading sessions directly from the editor to put your
    strategy into action.


### How a trading strategy in the tree looks

A trading strategy in Bee Algo includes the following information and
key components.

- **General Information**: Includes the name, description, tags, and
  corresponding tree data.

- **Tree Data**: The algorithms is configured and visualized in a tree
  view. The tree components are built to not only cover condition
  configurations for trading indicators/patterns but also the allocation
  weight and assets for specific buy/sell action. The following are main
  components in the tree:![A screenshot of a computer Description
  automatically

- **Group**: Like a block, is to group by sub-groups or the list of
  conditions and actions belongs to it. If there're more than one group,
  user can specify the weight for each group

- **Weight**: Define the weight of investment for each buy/sell action
  that's belonged it

- **Asset Block**: The asset is to use for buy/sell signal

- **If/Else** (Condition): is to define the buy/sell conditions from the
  technical indicators and their parameters.

- **Actions**: is to make decisions for specific signal: Buy or Sell


Each above component requires a name and the corresponding
**condition/ parameters

- Component: Asset Block
  -  Conditions/Parameters: Symbol - (Required block)
- Component: Weight
  - Conditions/Parameters: Allocation Percentage [unit: %] (Optional block). If no definition, the default value is 100%)
- Component: Action
  - Conditions/Parameters: (Required block)
  - Including the following configuration:
    - Order Type [Market]
    - Order Direction [Buy, Sell]
    - Symbol
    - Toggle (Percentage): Allows the user to specify the quantity for the order either by a fixed number or as a percentage of the trading account's assets/investment cash for buying, and a percentage of the holdings in the portfolio for selling.
      - If: Toggle = Off: The quantity is fixed for buy/sell.
      - If: Toggle = On: The quantity is set as a percentage for buy/sell based on the associated assets and portfolio
- Component: If//Else 
  - Conditions/Parameters: (Required block)
  - AND/OR: Set the combination rule for multiple conditions
  - A Condition configuration include:
    - 1st Indicators and corresponding parameters
    - Operator (Greater than/Less than/Equal/Cross Over/Cross Under]
    - 2nd indicator OR a fixed value, that’s used to compared to 1st indicator
    - Supported a variety of trading indicators and patterns

### 4 Steps to build a trading strategy

To easier and faster to create a trading strategy in Bee Algo, user can
use AI Assistant. After clicking on "Create new strategy" button, in the
creation editor, let's follow these steps:

- Step 1: Describe your desired strategy to the AI.

  - By clicking on the button "**Generate with AI"** in the root group
    of tree view which likely automates strategy generation based on
    predefined or learned indicators and parameters. In this screen,
    tell AI what you want to build
> For example: Create a trading strategy for BNBUSDT assets as follows: Buy when the price is above the EMA and the RSI is above 50. Sell when the price is below the EMA and the RSI is below 50*

- Step 2: Review the generated tree view with explanations.

  - AI will automatically return a strategy data response as the tree
    view and an explanation for that tree data. So that manual review is
    necessary

- Step 3: Use the AI-generated tree data to make further edits as needed
  in each component.

  - If user wants to use the tree data returned from AI, clicking on
    "Use this", AI suggested strategy will be filled into the tree
    editor.

  - Next steps: User can add new or edit or delete the data for each
    component in the tree editor. Refer to section: "How a trading
    strategy in the tree looks" to get more detailed the components
    configuration in this step

- Step 4: Confirm general information (name, description, tags) and save
  the strategy

### Trigger Back-test on Bee Algo

Once the user can save the strategy successfully, this means the
algorithm configuration is valid, ready for running the back test or
live trade.

Backtest Setups:

To run a backtest from a trading strategy, user need to define the
parameters for backtesting first, this section allows you to:
- From Date: Select the start date for backtest (e.g., January 1, 2021).
- To Date: Select the end date for backtest (e.g., December 31, 2023).
- Investment: Input the total capital you want to allocate for the strategy during the backtest.


When the parameters are set, click "**Run Backtest"** to simulate the
strategy based on selected historical data

The backtest will be proceed during main 3 steps:

- Step 1: Loading the data. Note: Currently, the system only supports
  the data resolution daily, make sure the parameters of used technical
  indicators are daily
- Step 2: Request the backtest. Using the conditions defined in tree
  view, run with the historic trading data.
- Step 3: Wait and visualize the backtest result (statistic key, charts,
  order)

Optional: If user want to share this backtest result and strategy to the community, clicking on "Publish to Market Place" button in the Overview tab. This step is optional


Detailed Backtest Result

There're 3 tabs are displayed in Backtest Result:

- Overview
  - Overview statistic:
    - Equity: The total portfolio value of all the holdings was sold at
      current market rates.
    - Fees: The total quantity of fees paid for all the transactions.
    - Holdings: The sum of all items in the portfolio
    - Return: The rate of return across the entire trading period
    - Unrealized: The amount of profit a portfolio would capture if it
      liquidated all open positions and paid the fees for transacting
      and crossing the spread.
  - Charts: Some of the build--in charts are shown to help users analyze
    performance of the algorithm.
    - Equity: Time series of equity and daily performance.
    - Exposure: Time series of long and short exposure ratios. This
      chart indicates the risk of the strategy, the bigger the gap
      between 2 ratios, the higher the risk is.
  - Overall Key Statistics: Here is the description of each component in
    the statistics table

| **PSR**                                                                    | The probability that the estimated Sharpe ratio of an algorithm is greater than a benchmark.                                                           |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Sharpe Ratio**                                                           | A measure of the risk-adjusted return, developed by William Sharpe.                                                                                    |
| **Total Trades**                                                           | The number of orders that were filled or partially filled.                                                                                             |
| **Average Win**                                                            | The average rate of return for profitable trades.                                                                                                      |
| **Average Loss**                                                           | The average rate of return for unprofitable trades.                                                                                                    |
| **Compounding Annual Return**                                              | The annual percentage return that would be required to grow a portfolio from its starting value to its ending value.                                   |
| **Drawdown**                                                               | The largest peak to trough declines in an algorithm's equity curve.                                                                                    |
| **Expectancy**                                                             | The expected return per trade.                                                                                                                         |
| **Net Profit**                                                             | _(Percent)_ The rate of return across the entire trading period.                                                                                       |
| _(Dollar-value)_ The dollar-value return across the entire trading period. |
| **Loss Rate**                                                              | The proportion of trade that was not profitable.                                                                                                       |
| **Win Rate**                                                               | The proportion of trade that was profitable.                                                                                                           |
| **Profit-Loss Ratio**                                                      | The ratio of the average win rate to the average loss rate.                                                                                            |
| **Alpha**                                                                  | The quantity of an algorithm's returns isn't explained by its underlying benchmark.                                                                    |
| **Beta**                                                                   | The scale and direction of an algorithm's returns relative to movements in the underlying benchmark.                                                   |
| **Annual Standard Deviation**                                              | A statistical measure that describes the dispersion of annual returns relative to the mean annual return. It's the square root of the annual variance. |
| **Annual Variance**                                                        | A statistical measure that describes the dispersion of annual returns relative to the mean annual return.                                              |
| **Information Ratio**                                                      | The number of excess returns from the risk-free rate per unit of systematic risk.                                                                      |
| **Tracking Error**                                                         | A measure of how closely a portfolio follows the index to which it is benchmarked. A tracking error of 0 is a perfect match                            |
| **Treynor Ratio**                                                          | A measurement of the returns earned in an algorithm in excess of the risk-free rate per unit of benchmark risk, developed by Jack Treynor.             |
| **Total Fees**                                                             | The total quantity of fees paid for all the transactions.                                                                                              |
| **Estimated Strategy Capacity**                                            | The maximum amount of money an algorithm can trade before its performance degrades from market impact.                                                 |
| **Lowest Capacity Asset**                                                  | The asset an algorithm traded that has the lowest capacity.                                                                                            |

- Orders: The list of virtual orders that's triggred during the backtest

- Error Logs: Logs tab displays the error logs of the backtest if any
  issue happens

### Trigger a live trade process for a trading strategy:

In strategy details, clicking **Live Trading** to start executing the
strategy in real-time using actual payable assets & current portfolio of
selected account.

Live trading result will display real-time in the live trade tab. The
live trading result are like backtest result, but the differences are:

- Actual Orders & Real-time Equity: Based on the algorithm of the
  strategy, the system will place orders that are executed in real-time
  in the market. Live trading involves real money, meaning any gains or
  losses impact the user's account actual funds.

- Real-time Orders and Backtest logs

When user want to cancel the live trading, clicking on "Stop" to cancel
the process

## Bee Marketplace 

From Bee Algo, user can share your trading strategy and performance
result from backtest to the Beelab community. All user's able to access
shared trading strategies. These strategies include algorithms data
under a tree structure, along with performance metrics from their back
testing results.


With the supported two view modes, users can browse the list of shared
strategies using a comprehensive filter with dynamic combinations to
filter by performance metric values. User can also customize the data
displayed in the list

To view the details of a strategy, click on a record to be redirected to
the detailed page, as shown in the following screenshot

Users can clone a strategy to edit or further enhance them by clicking
on "Clone"

## Bee Portfolio 

This module helps user to manage total assets and portfolios across all
client and associated trading accounts.

- Total assets are aggregated daily to reflect changes, with options to
  filter by specific brokerages and accounts.

- Portfolio charts display the holdings, including the number of stocks,
  symbols, and their percentage contributions to the user\'s overall
  portfolio in Bee.

