# Firewall Configuration

## 1. Firewall Configuration

### Allow SSH

```bash
sudo ufw allow ssh
```

### Default Deny Policy

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

### Allow Port 8080 (Web Application)

```bash
sudo ufw allow 8080/tcp
```

## Verification

Check the rules and confirm the web application responds locally:

```bash
sudo ufw status numbered
curl http://localhost:8080/
```

Resulting rules:

| # | To | Action | From |
|---|----|--------|------|
| 1 | 22/tcp | ALLOW IN | Anywhere |
| 2 | 8080/tcp | ALLOW IN | Anywhere |
| 3 | 22/tcp (v6) | ALLOW IN | Anywhere (v6) |
| 4 | 8080/tcp (v6) | ALLOW IN | Anywhere (v6) |

The `curl` request returned the default "Welcome to nginx!" page, confirming the web server is running and reachable on port 8080.

## What happens if `ufw enable` runs before `ufw allow ssh`?

Running `sudo ufw enable` before allowing SSH would immediately block all
incoming traffic, including the active SSH connection, locking the
administrator out of the server with no way back in except through the
cloud provider's emergency console.
