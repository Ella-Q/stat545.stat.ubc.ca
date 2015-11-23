You can see the glorious result of all this by visiting the `foofactors` package on GitHub: <https://github.com/jennybc/foofactors>.

back to [All the package things](packages00_index.html)

**!! Modify the path below to create your new package where YOU want it on YOUR system !!** Use RStudio's auto-completion of paths to make sure the path actually exists. To avoid nesting a Git repo within a Git repo, do NOT put this inside your STAT 545 repository. Do NOT put this inside any directory that is already a Git repository. Directly or indirectly.
What does it look like? Here's a file listing (locally, you can consult your file browser):
  * The `R/` directory is the ["business end" of your package](http://r-pkgs.had.co.nz/r.html). It will soon contain `.R` files with function definitions.


#> [38ed51b] 2015-11-23: Initial commit
FYI RStudio can also initialize a Git repository, in any Project, even if it's not an R package: *Tools > Version Control > Project Setup*. Then choose *Version control system: Git* and *initialize a new git repository for this project*.
Learn the keyboard and menu shortcuts for this. In RStudio:
We can all think of lots of ways to improve `fbind()`. Or maybe you can think of more urgent factor fires that you would like to put out. That's why we have [homework](hw10_package.html)!
Your most recent commit should look something like this (if you're lucky, you've got a nicer way of inspecting it):
#> [39cb828] 2015-11-23: Add fbind()
#> diff --git a/R/fbind.R b/R/fbind.R
#> new file mode 100644
#> index 0000000..7b03d75
#> --- /dev/null
#> +++ b/R/fbind.R
#> @@ -0,0 +1,3 @@
#> +fbind <- function(a, b) {
#> +  factor(c(as.character(a), as.character(b)))
#> +}
We could simply try to install and load the package and hope for the best. Recall this figure from [R Packages](http://r-pkgs.had.co.nz/package.html):

Just this once, run `check()` with `document = FALSE`, so we don't get ahead of ourselves. (Specifically, I don't want to mess with our `NAMESPACE` file yet.)

At this point, you should expect to get two warnings:

  * `Non-standard license specification`
  * `Undocumented code objects: 'fbind'`
  
We'll fix both soon.
check(document = FALSE)
#>   '/var/folders/vt/4sdxy0rd1b3b65nqssx4sx_h0000gn/T//RtmpX4V9Xx/foofactors_0.0.0.9000.tar.gz'  \
#### Did it really work?

Now that we've installed `foofactors` properly, let's revisit our small example.


```r
library(foofactors)
a <- factor(c("character", "hits", "your", "eyeballs"))
b <- factor(c("but", "integer", "where it", "counts"))
fbind(a, b)
#> [1] character hits      your      eyeballs  but       integer   where it 
#> [8] counts   
#> Levels: but character counts eyeballs hits integer where it your
```

Success! That's enough for now.
In [part two](packages05_foofactors-package-02.html), we'll add more bells and whistles to the package.
<!--http://davidgohel.github.io/ReporteRs/FlexTable.html-->