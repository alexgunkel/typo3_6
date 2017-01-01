FROM php:5.6-cli
MAINTAINER alexandergunkel@gmail.com

ADD crontab /etc/cron.d/TYPO3
RUN chmod 0644 /etc/cron.d/TYPO3

RUN touch /var/log/cron.log

RUN apt-get update && apt-get install -y cron
CMD cron && tail -f /var/log/cron.log
