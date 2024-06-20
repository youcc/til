### Convert all text in a data frame to uppercase
```
df %>%
  mutate_all(funs(upper))
```
