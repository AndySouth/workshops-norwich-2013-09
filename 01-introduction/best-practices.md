
# Some best practices for using R

1. Manage all of your source files for a project in the same directory. Then use relative paths as necessary. For example, use

```
df <- read.csv(file = "/files/dataset-2013-01.csv", header = TRUE)
```

rather than:

```
df <- read.csv(file = "/Users/Karthik/Documents/sannic-project/files/dataset-2013-01.csv", header = TRUE)
```

2. Never change the working directory once a script is underway. Use `setwd()` first . Do it at the beginning of a R session. Better yet, start R inside a project folder.

3. Don't save a session history (the default option in R). Instead, start in a clean environment so that older objects don't contaminate your current environment. This can lead to unexpected results, especially if the code were to be run on someone else's machine.

4. Where possible attach `sessionInfo()` somewhere in your project folder. Session information is invaluable since it captures all of the packages used in the current project. If a newer version of a project changes the way a function behaves, you can always go back and reinstall the version that worked (Note: At least on CRAN all older versions of packages are permanently archived).

When you use the `stitch()` function in the `knitr` package, it automatically includes this information.



