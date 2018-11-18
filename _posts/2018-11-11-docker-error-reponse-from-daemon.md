---
published: true
tags: docker
---
## "Error response from daemon"

I recently tried installing docker community edition on Mac but ran into an issue when trying to run the 'Hello World' test procedure.

```
Error response from daemon: 
Get https://registry-1.docker.io/v2/: 
unauthorized: incorrect username or password
```

I found that I needed to set my credentials using my *userid* instead of my email by running the following command

```
docker login
```

(Your login id can be found in your docker account and/or system tray icon)
