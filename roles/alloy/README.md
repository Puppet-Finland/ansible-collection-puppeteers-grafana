# Puppeteers Grafana Alloy Role
This is a wrapper role around the [grafana.grafana.alloy](https://galaxy.ansible.com/ui/repo/published/grafana/grafana/content/role/alloy/) role.
The purpose of this, is to dynamically build custom alloy configuration templates for our purposes.

The official documentation for alloy configuration in the loki context can be found [here](https://grafana.com/docs/alloy/latest/reference/components/loki/loki.source.file/#lokisourcefile).

## Required Values and their defaults
```yaml
  puppeteers_grafana_alloy_loki_endpoint_url: http://loki.example.com:3100
  puppeteers_grafana_alloy_confd: /etc/alloy/conf.d
  puppeteers_grafana_alloy_loki_environment_extra_labels: {}
  puppeteers_grafana_alloy_loki_logs: {}
```

## Example log watching
```yaml
puppeteers_grafana_alloy_loki_logs:
  - service: example
    log_dir: "/var/log/example"
    log_pattern: "*.log"
    file_watch: true
```
