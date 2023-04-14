## syncthing-status

R script that checks for [Syncthing](https://syncthing.net/) connections and displays some output for use with [Polybar](https://github.com/polybar/polybar). Why use an overengineered R script for something that probably could be more easily achieved using Python or just plain Bash? Beacuse I want to get better at using R for general programming stuff :man_shrugging:.

## Usage

Download the script and make sure it's executable (`chmod +x syncthing_status.R`), and that you have the R packages [httr](https://cran.r-project.org/web/packages/httr/), [XML](https://cran.r-project.org/web/packages/XML/), [magrittr](https://magrittr.tidyverse.org/), [dplyr](https://dplyr.tidyverse.org/), and [stringr](https://stringr.tidyverse.org/) installed. You'll also need [Font Awesome](https://fontawesome.com/) if you want icons. Then add something like this to your `user_modules.ini`:

```
[module/syncthing]

type = custom/script
exec = "Rscript ~/syncthing-status/syncthing_status.R"
interval = 60
format = "<label>"
```
