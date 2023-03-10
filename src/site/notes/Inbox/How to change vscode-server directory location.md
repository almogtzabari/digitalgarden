---
{"dg-publish":true,"permalink":"/inbox/how-to-change-vscode-server-directory-location/","tags":[null]}
---



# How to change vscode-server directory location
Simply put the following in the `settings.json`:
```json
"remote.SSH.serverInstallPath": {
	"my_hostname.some_domain.com": "/path/to/directory"
}
```

Note that the key is the hostname is shown in the ssh config file, and the value is the location.
