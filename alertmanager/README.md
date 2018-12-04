A. Requirement to integrate with Monitoring Services

    a. alertmanager.aws.<your-company>.com      - in Route53
    b. An Ingress point 


B. General Notes

    a. Prometheus must be deployed before Alertmanager
    b. Prometheus reads alerts from ./ops/k8s/services/monitoring/charts/prometheus/resources/rules/alert.rules
    c. Following file links the alert.rules to promethus. See under 'alert.rules:'
        ./ops/k8s/services/monitoring/charts/prometheus/templates/prometheus-configmap.yml

    d. Emails are sent via mail.aws.axsy.com
    e. Slack alerts are sent out to my personnel channel. This requires changing according to the wishes
    of the operations team.


C. Issues:
   a. All the alerts must be in alert.rules file. I prefer to have individual or grouped files. This is possible
      as shown in my Mac setup.

      Alerts may be grouped according to, for example, serverity, system, application etc.
      Once we run the service for a while and start creating alerts, the operations team will get
      a feeling for the best way to group alerts.







