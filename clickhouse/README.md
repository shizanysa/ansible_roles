# Role for clickhouse install and configs


Example
---

clickhouse_conf:
  default_profile: "default"
  default_database: "default"
  logger:
    log: "/var/log/clickhouse-server/clickhouse-server.log"
    errorlog: "/var/log/clickhouse-server/clickhouse-server.err.log"
    size: "1000M"
  http_port: "8123"
  tcp_port: "9000"
clickhouse_users:
  users:
    test_user:
      password: "test_pass"
      profile: "default"
    default:
      password: ""
      profile: "default"

clickhouse_databases:
  - name: nginx
    state: present
  - name: web
    state: absent

---
