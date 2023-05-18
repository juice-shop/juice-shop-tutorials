# OWASP Juice Shop - Integration Tutorial

## Prerequisites

1. [Install OWASP Juice Shop](https://github.com/juice-shop/juice-shop#setup) locally. 
2. Open [OWASP Juice Shop - Tutorial Series - Integration.pdf](OWASP%20Juice%20Shop%20-%20Tutorial%20Series%20-%20Integration.pdf) for context and general instructions.

## Tutorial Steps

### 1. Challenges API
n/a

### 2. Challenges Declaration File
n/a

### 3. Direct Links
n/a

### 4. Challenge Solution Webhook
Set up a server that exposes a Webhook URL to listen for Juice Shop notifications.

For testing, you can for example [create a public RequestBin](https://public.requestbin.com/r).

Start Juice Shop while passing in the URL of your webhook via the `SOLUTIONS_WEBHOOK` environment variable, e.g. on Linux:

```
SOLUTIONS_WEBHOOK=<your webhook URL> npm start
```

Open your Juice Shop instance in another tab and start solving some challenges. You should get notifications for each solved hacking and coding challenge on the webhook.

### 5. Prometheus Metrics
n/a
