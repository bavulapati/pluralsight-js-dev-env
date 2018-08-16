> [Tools](./Tools-decisions.md)

# [Electron Log](https://github.com/megahertz/electron-log)
* Logger will use info level for file
* Max file size will be 128 KB
* If the file size crosses the max size, it will be saved in log.old.log
* Log file for linux will be at ~/.config/remotepc/log.log
* We need to import the logger as log in the file we need to use