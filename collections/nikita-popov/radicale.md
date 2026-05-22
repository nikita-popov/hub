Defend [Radicale](https://radicale.org/) CalDAV/CardDAV instances against brute-force and credential stuffing attacks.

Includes:
- Radicale access log parser
- Brute-force / credential stuffing scenario

## Acquisition template

```yaml
***
source: file
filenames:
  - /var/log/radicale/radicale.log
labels:
  type: radicale
```

**Journald variant (systemd unit `radicale.service`):**

```yaml
***
source: journald
journalctl_filter:
  - "_SYSTEMD_UNIT=radicale.service"
labels:
  type: radicale
```
