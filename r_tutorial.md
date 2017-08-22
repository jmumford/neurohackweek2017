# R tutorial
Jeanette Mumford  

## Installing R and getting started
[R](https://www.r-project.org/) is free and I highly recommend using R through the IDE, [RStudio](https://www.rstudio.com/), which offers a lot of helpful functionality like generating R markdown files easily and integrating with git.  A common confusion is updating RStudio is \emph{not} also updating R as they are separate programs.

To install R and RStudio, start by installing R and then install RStudio second.  RStudio should automatically find R when it installs.

Like Python, R requires installing libraries for more advanced tools, but unlike Python the installation is typically very easy.  Most libraries you will want to use are located in the [CRAN](https://cran.r-project.org/) (Comprehensive R Archive Network), which can be accessed through R, directly.  The following illustrates how you'd install and load a package.



```r
# <-  The comment in R is the hash symbol

# To grab libraries for installation, R will ask you to
# select a CRAN "mirror".  The following line will set the
# mirror permanently so R doesn't ask you over and over again.
#  All the mirrors are listed here: https://cran.r-project.org/mirrors.html

# You only need to run this once ever (not once per session)
options(repos=structure(c(CRAN="http://cran.us.r-project.org")))


# To install a library use the following, note double quotes are used.
# A "newer" feature is dependencies (libraries the library of 
# interest needs) will automatically be installed.

# You only need to run this once ever (not once per session)
#install.packages("ggplot2")

# To load the library so you can access the functions 

# Run once per session if you'd like to use it
library("ggplot2")
```

```
## Warning: package 'ggplot2' was built under R version 3.3.2
```

For the above you will likely get more output than I did when you run install.packages, as I already had it installed.

Now open a new editor (in RStudio click the white page icon in the upper left and select, "R Script", and we'll write a quick "hello world".  Enter the following in the file and save it in a file called "first_script.R".

```r
print("Hello world")
```

I feel it is poor coding form to change working directories, so I always recommend typing out the full paths to files.  So edit the following to reflect where you just stored your file.  This will run your script.

```r
source("/Users/jeanettemumford/Documents/Research/Teaching/neurohackweek2017/first_script.R")
```

```
## [1] "Hello world"
```

If you want to run the script from the LINUX prompt you would use "Rscript first_script.R"
