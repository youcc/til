# r-tips
Tricks I've learned in using R

### Convert all text in a data frame to uppercase
```
df %>%
  mutate_all(funs(upper))
```

### Replace string 
```
df$column <- str_replace(df$column, "GENERAL", " ")) 
```
