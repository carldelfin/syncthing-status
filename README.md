## syncthing-status

R script that checks for [Syncthing](https://syncthing.net/) connections, and displays output for use with [Polybar](https://github.com/polybar/polybar).

## Usage

Download the script and make sure it's executable (`chmod +x syncthing_status.R`). Add the following your `polybar.conf`:

```
[module/syncthing]

type = custom/script
exec = "Rscript ~/dotfiles/scripts/syncthing_status.R"
interval = 60
format = "<label>"
```

asd.
