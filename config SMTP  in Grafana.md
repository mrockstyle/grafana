# Setup SMTP TN in Grafana
- ### Edit flie "grafana.ini"
    ```
    vi /etc/grafana/grafana.ini
    ```
    ```
    [smtp]
    enabled = true
    host = 10.220.109.45:25
    ;user =
    # If the password contains # or ; you have to wrap it with trippel quotes. Ex """#password;"""
    ;password =
    ;cert_file =
    ;key_file =
    skip_verify = true
    from_address = no-reply@tnis.com
    from_name = Grafana
    # EHLO identity in SMTP dialog (defaults to instance_name)
    ;ehlo_identity = dashboard.example.com
    ```
- ### Restart service grafana
    ```
    systemctl restart  grafana-server 
    systemctl status  grafana-server
    ```
