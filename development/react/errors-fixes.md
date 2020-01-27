No. | Error | Fix |
:---:| :---: | :---: |
1 | "Error: ENOSPC: System limit for number of file watchers reached" | `echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p` |
2 | something | something |