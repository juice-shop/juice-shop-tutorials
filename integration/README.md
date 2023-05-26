# OWASP Juice Shop - Integration Tutorial

## Prerequisites

1. [Install OWASP Juice Shop](https://github.com/juice-shop/juice-shop#setup) locally. 
2. Open [OWASP Juice Shop - Tutorial Series - Integration.pdf](OWASP%20Juice%20Shop%20-%20Tutorial%20Series%20-%20Integration.pdf) for context and general instructions.

## Tutorial Steps

### 1. Challenges API
n/a

**Example Integrations**
* <https://www.npmjs.com/package/juice-shop-ctf-cli>
* <http://juice-shop.github.io/juice-shop/#/5> (challenge count in slide title)

### 2. Challenges Declaration File
n/a

**Example Integrations**
* <https://owasp-juice.shop/> project website populates its [Challenge Categories](https://owasp.org/www-project-juice-shop/#div-challenges) and [Hacking Instructor Tutorials](https://owasp.org/www-project-juice-shop/#div-tutorials) tables from the `master` YAML file
* [OpenCRE importer](https://github.com/OWASP/common-requirement-enumeration/blob/main/application/utils/external_project_parsers/juiceshop.py) maps challenges as training resources to then show on <https://opencre.org>
* Challenge Solution Webhook (see 4.)

### 3. Direct Links
n/a

**Example Integrations**
* Juice Shop challenges as training resource links on <https://opencre.org>, e.g.

```
Tool : OWASP Juice Shop : localXssChallenge : DOM XSS
Reference: https://demo.owasp-juice.shop/#/score-board?challenge=DOM%20XSS
```

### 4. Challenge Solution Webhook
Set up a server that exposes a Webhook URL to listen for Juice Shop notifications.

For testing, you can for example [create a public RequestBin](https://public.requestbin.com/r).

Start Juice Shop while passing in the URL of your webhook via the `SOLUTIONS_WEBHOOK` environment variable, e.g. on Linux:

```
SOLUTIONS_WEBHOOK=<your webhook URL> npm start
```

Open your Juice Shop instance in another tab and start solving some challenges. You should get notifications for each solved hacking and coding challenge on the webhook.

**Example Integrations**
* <https://github.com/juice-shop/multi-juicer> team scoreboard

### 5. Prometheus Metrics
n/a

**Example Integrations**
* <https://github.com/juice-shop/multi-juicer> provides a Grafana dashboard to the admin for team progress tracking and troubleshooting instances
* A RaspberryPi under Björn‘s desk scrapes <http://demo.owasp-juice.shop/metrics> and hosts [a Grafana dashboard](https://github.com/juice-shop/juice-shop/blob/master/monitoring/grafana-dashboard.json)
