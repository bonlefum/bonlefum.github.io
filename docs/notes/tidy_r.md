# Plotting in R

ggplot has an interesting formalism for graphing that is quite different from the object-oriented matplotlib approach, at least superficially.

## How to order presentation of the data

``The order of the rows in a dataframe should have no influence on the plot; anything else is a bug'' (paraphrasing from a forum entry I can't seem to find again). 

Surprising how much effort some small things can take...

With dplyr we can easily sort data with `arrange(col1, col2)`, but ggplot then
takes alphabetical ordering over string data.  One workaround is to turn
strings into a factor, e.g. in a dplyr pipeline, `data %>% arrange(-counts) %>%
mutate(Position = factor(Position, Position)) %>%` [SO
post](https://stackoverflow.com/a/38663292).  This works ok if the strings
appear precisely once (e.g. in a bar plot, after the data has been grouped or
summarised).  But if the data retains multiple entries of a value (e.g. for use
in a boxplot) it is not possible to cast it into a factor.  Here, we can use
the reorder function within setting the aesthetic, e.g., `ggplot(tips2, aes(x =
reorder(day, -perc), y = perc)) + geom_bar(stat = "identity")` as shown in this
[gh page](https://sebastiansauer.github.io/ordering-bars/).

How would I approach it in mpl? Set the index as the sort order, then define
the data and respective labels by indexing into the original dataset.


