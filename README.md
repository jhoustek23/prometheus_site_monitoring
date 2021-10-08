# prometheus_site_monitoring

Instant http(s) site monitoring with cert validity and slack notifications.


change those files:

alertmanager/alertmanager.yml

global section:
 slack_api_url: "https://hooks.slack.com/services/XXXXXXX"

recievers section:
  - username: 'Alertmanager'
  - api_url: 'https://hooks.slack.com/services/XXXXXXXX'
  - channel: '#alertmanager'

prometheus/blackbox-targets.yml

Then just run docker-compose up -d and your instance will be on 0.0.0.0:9090 firing alerts to Slack channel.
