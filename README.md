# URL Sentry - URL Monitoring and Management CLI

- "URL Sentry" is a Python CLI tool for monitoring URL data, including status code, title, JS files, and content length.
- It allows users to add, remove, and view URL data in a simple and convenient way.

### Installation

1. Clone the repository:

```bash
git clone https://github.com/H3lllfir3/URL_Sentry.git
cd URL_Sentry
```

2. Install the CLI globally:

```bash
pip install -e .
```

### Scheduling Using a Cron Job

- The script runs automatically every 1 hour.

### Sending Notifications

- Users can enable notifications for important events by setting up a Discord webhook URL.
- To set the webhook URL, use the following command:

```bash
url-sentry --set_hook WEBHOOK-URL
```

### Usage

#### Add URL Data

To add URL data, use the following command:

```bash
url-sentry add -u <url> [options]
```

Available options:
- `-status-code`: Include status code.
- `-title`: Include title.
- `-js`: Include JS files.
- `-content-length`: Include content length.

Examples:

```bash
url-sentry add -u domain.tld -content-length
url-sentry add -u domain.tld -title
url-sentry add -u domain.tld -status-code -js
```

#### Remove URL Data

To remove URL data, use the following command:

```bash
url-sentry remove -u domain.tld
```

#### View Logs

To view the logs, use the following command:

```bash
url-sentry -logs
```

#### View All Records

To view all URL records, use the following command:

```bash
url-sentry -subs | jq
```

### Contributing

- Contributions are welcome! Users can open issues or submit pull requests for bug fixes or improvements.

### License

- This project is licensed under the MIT License, allowing free use, modification, and distribution for personal and commercial purposes.

Overall, the README provides clear instructions and examples on how to use the "URL Sentry" CLI tool, making it easy for users to get started and contribute to the project if they wish.