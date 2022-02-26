## syncthing-status

R script that checks for [Syncthing](https://syncthing.net/) connections and displays some output for use with [Polybar](https://github.com/polybar/polybar). Why use an overengineered R script for something that probably could be more easily achieved using Python or just plain Bash? Beacuse I want to get better at using R for general programming :man_shrugging:.

## Usage

Download the script and make sure it's executable (`chmod +x syncthing_status.R`). Make sure you have [httr](https://cran.r-project.org/web/packages/httr/), [XML](https://cran.r-project.org/web/packages/XML/), [magrittr](https://magrittr.tidyverse.org/), [dplyr](https://dplyr.tidyverse.org/), and [stringr](https://stringr.tidyverse.org/) installed. You'll also need [Fontawesome](https://fontawesome.com/) installed. Then add something like the following your `polybar.conf`:

```
[module/syncthing]

type = custom/script
exec = "Rscript ~/dotfiles/scripts/syncthing_status.R"
interval = 60
format = "<label>"
```
