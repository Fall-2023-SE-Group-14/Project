<p align="center">
  <img src="./docs/dollar_bot.jpg" alt="Expense tracking made easy!" width="600">
</p>

<div align="center">

  [![MIT license](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
  [![Style Checker](https://github.com/Fall-2023-SE-Group-14/DollarBot/actions/workflows/styleChecker.yml/badge.svg)](https://github.com/Fall-2023-SE-Group-14/DollarBot/actions/workflows/styleChecker.yml)
  [![Platform](https://img.shields.io/badge/Platform-Telegram-blue)](https://desktop.telegram.org/)
  [![GitHub](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
  [![GitHub contributors](https://img.shields.io/github/contributors/Fall-2023-SE-Group-14/DollarBot)](https://github.com/Fall-2023-SE-Group-14/DollarBot/graphs/contributors)
  [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10198249.svg)](https://doi.org/10.5281/zenodo.10198249)
  [![Build Status](https://app.travis-ci.com/sak007/MyDollarBot-BOTGo.svg?branch=main)](https://app.travis-ci.com/github/sak007/MyDollarBot-BOTGo)
  [![codecov](https://codecov.io/gh/sak007/MyDollarBot-BOTGo/branch/main/graph/badge.svg?token=5AYMR8MNMP)](https://codecov.io/gh/sak007/MyDollarBot-BOTGo)
  [![GitHub open issues](https://img.shields.io/github/issues/Fall-2023-SE-Group-14/DollarBot)](https://github.com/Fall-2023-SE-Group-14/DollarBot/issues?q=is%3Aopen+is%3Aissue)
  [![GitHub closed issues](https://img.shields.io/github/issues-closed/Fall-2023-SE-Group-14/DollarBot)](https://github.com/Fall-2023-SE-Group-14/DollarBot/issues?q=is%3Aissue+is%3Aclosed)
  ![Fork](https://img.shields.io/github/forks/Fall-2023-SE-Group-14/DollarBot?style=social)

</div>

# 💰 DollarBot - Budgeting On The Go 💰

DollarBot is your easy-to-use Telegram Bot that simplifies recording daily expenses on a local system with simple commands. Manage your expenses effortlessly, allowing you to:
- Add/Record new spending
- Calculate the sum of your expenditure for the current day/month
- Display your spending history
- Clear/Erase all your records
- Edit/Change any spending details if needed
- Recurring expense: Add a recurring expense that adds a certain amount every month to the user's spending, for any given category.
- Custom category: Add a new category and delete an existing category as needed
- Budgeting: View the budget value for total expenses and/or for each existing category in the /display function
- Better visualization: Added pie charts, bar graphs with and without budget lines for a better look at spending history
  Added a bar graph in the /history command to see spending across different categories
  View daily and monthly expenses for spending history


> Where simplicity converges with financial harmony, right at your fingertips.

<div style="display: flex; align-items: center;">
  <div>

  <img src="./DollarBotDemoNewGIf.gif" alt="Dollar Bot" width="200" style="margin-right: 20px;"/>

  </div>
  <div>

  ## What's New?!

  With just a few quick commands, DollarSplitBot provides you with the ability to:

  1. **Welcome New Companions:** Easily add your friends to simplify expense sharing.
  2. **Record Your Transactions:** Effortlessly document and store your expenses.
  3. **Fair Divisions:** Unveil your spending history, clarifying who owes what to whom.
  4. **Financial Insights:** Monitor your daily and monthly expenditure totals.
  5. **Your Financial Narrative:** Retrieve your spending history whenever you need it.
  6. **A Fresh Start:** Clear all records when it's time to begin anew.
  7. **Customized Details:** Modify any spending details according to your preferences.
  8. **Document Trail:** Generate polished PDF expenditure reports for a comprehensive overview.
  9. **Friendly Reminders:** Send amiable email reminders to ensure financial settlements.
  10. **Invoice OCR:** You can just scan your bill and get the data automatically added to the app.
  </div>
</div>


## Table of Contents

- [Demo](#demo)
- [Installation](#installation)
  - [Pre-requisites](#pre-requisites)
  - [Actual installation](#actual-installation)
  - [Testing](#testing)
  - [Code Coverage](#code-coverage)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Support](#support)
- [FAQs](#faqs)
- [Changelogs](#changelogs)
- [Code of Conduct](#code-of-conduct)

## Installation

### Pre-requisites

Here are some pre-requisites that you'll need to take care of before starting installation:
1. In the Telegram App/Desktop, search for "BotFather". Click on "Start" and enter the following command:

```
/newbot
```

2. Follow the instructions on the screen:
    a. Choose a name for your bot.
    b. Select a username for your bot that ends with "bot" (this is a rule from Telegram's side)

3. BotFather will confirm the creation of your bot and provide an HTTP API access token.
4. Copy and save this token for future use.

### Actual Installation

To install all the required libraries in a separate virtual environment, follow the commands below:
1. Create a virtual environment:
    ```
    python -m venv venv
    ```
2. Activate the virtual environment:

    On Windows:
    ```
    .\venv\Scripts\activate
    ```

    On Unix or MacOS:
    ```
    source venv/bin/activate
    ```

Follow these instructions to set up this bot on your end in just a few minutes:

1. Clone this repository to your local system.
2. Start a terminal session in the directory where the project has been cloned. Run the following command to install the required dependencies:
  ```
  pip install -r requirements.txt
  ```

3. In the directory where this repo has been cloned, run the following command to execute a bash script to run the Telegram Bot:
  ```
  ./run.sh
  ```

(OR)

  ```
  bash run.sh
  ```

4. Paste the API token you received from Telegram in pre-requisites step 4 when prompted.
5. A successful run will generate a message on your terminal that says "TeleBot: Started polling."

6. In the Telegram app, search for your newly created bot by entering the username and open the same. Now, on Telegram, enter the "/start" or "/menu" command, and you are all set to track your expenses!

## Configuring Email Credentials for SMTP: Sending Emails from Your Account

**SMTP (Simple Mail Transfer Protocol)** is a standard protocol for sending emails. It is widely used for sending email messages from one server to another. In the code, we are using SMTP to send emails via a Gmail account. Here's how the SMTP configuration and usage work:

1. **SMTP Server**: The `smtp_server` variable is set to 'smtp.gmail.com,' which is the SMTP server for Gmail. This server is responsible for sending your email messages.

2. **SMTP Port**: The `smtp_port` variable is set to 587. This is the port for TLS (Transport Layer Security) encryption. Gmail uses this port for secure email communication.

3. **SMTP Username**: The smtp_username variable should be set to your own Gmail email address from which you want to send the emails. Make sure to replace `your-email@gmail.com` with your actual Gmail email address in the code. This ensures that the emails will be sent from your specific Gmail account.

4. **SMTP Password**: The `smtp_password` variable is set, you need to generate an "App Password". An App Password is a 16-character code that allows you to access your Gmail account without revealing your real password. To generate an App Password, follow these steps:

   - Go to your Google Account settings (https://myaccount.google.com/).
   - In the "Security" section, under "Signing in to Google", select "App Passwords".
   - Select "Mail" and "Other (Custom name)" from the dropdown menus.
   - Click "Generate".
   -  Google will provide you with a 16-character App Password. Use this as your `smtp_password` in your code.

By customizing these settings, you can send emails from any email account using SMTP. Just ensure you are adhering to the security guidelines provided by your email provider.

### Testing

We use pytest to perform testing on all unit tests together. The command needs to be run from the home directory of the project. The command is:

```
python run -m pytest test/
```

(OR)

```
python -m pytest test/
```


### Code Coverage

Code coverage is part of the build. Every time new code is pushed to the repository, the build is run, and along with it, code coverage is computed. This can be viewed by selecting the build, and then choosing the codecov pop-up on hover.

Locally, we use the coverage package in python for code coverage. The commands to check code coverage in python are as follows:

```
coverage run -m pytest test/
```

```
coverage report
```


## Usage

We have tried to make this application (bot) as easy as possible. It's pretty self-explanatory. You can use this bot to manage and track your daily expenses and not worry about losing track of your expenses. As we have also given in functionality for graphing and plotting and history of expenses, it becomes easy for the user to track expenses.

## Configuration

As a user, there's no need to configure any parameters. As a contributor, we have tried to make the system as decoupled as possible so that changes to one module/program don't affect other ones. With this being said, here are some configuration knobs that we have exposed for contributors:
1. Adding categories,
2. Removing categories,
3. Graphing changes,
4. Changing Telegram bot names, etc.

## Contributing

Thank you for your interest in contributing to DollarBot! Your contributions are highly valued, and this document will help you get started with the process.
We have a fully detailed comprehensive document to look out for if you're looking into contributing towards this project!
Please refer to this [CONTRIBUTING.md](CONTRIBUTING.md) file.

## LICENSE

By contributing to DollarBot, you agree that your contributions will be licensed under the project's open-source license. It's important to understand and respect the licensing terms before contributing. The specific license terms for this project can be found in the [LICENSE](LICENSE) file.

## Acknowledgements

Here is a section where we will acknowledge the contributors to this project (sorted alphabetically):
- Harini Ravi
- Jay Vishaal Janarthanan
- Manasi Bhagwat
- Zahra Shiraz

## Support

[Add here]

## FAQs

1. Will we need a Telegram account to run this?
    A. Yes

2. Will we have to run multiple instances of the server for multiple clients?
    A. No

3. How can we reach out to the developers/contributors?
    A. Look out for the contributors/active developers and contact them.

4. What if I encounter a bug/have a feature request?
    A. File in an Issue, and then we can discuss further!

## Changelogs

[Add here]

## Code of Conduct

Please note that we have a [Code of Conduct](CODE_OF_CONDUCT.md) that all contributors are expected to follow. It ensures that our community is welcoming and inclusive.

## What more can be done?

Please refer to the issue list available [here](https://github.com/Fall-2023-SE-Group-14/DollarBot/issues) to see what more can be done to make MyDollarBot better. Please refer to the MyDollarBot project present [here](https://github.com/orgs/Fall-2023-SE-Group-14/projects/2/views/1) to have a look at the tasks to be done, tasks currently in progress, and tasks already done.

## Demo

You can view the demo [here](https://youtu.be/EX9CTIBbOuc)

</div>
