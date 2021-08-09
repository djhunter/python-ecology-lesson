This section will use the `surveys.csv` file that can be downloaded here:
[https://ndownloader.figshare.com/files/2292172][figshare-ndownloader]

| Column           | Description                        |
|------------------|------------------------------------|
| record_id        | Unique id for the observation      |
| month            | month of observation               |
| day              | day of observation                 |
| year             | year of observation                |
| plot_id          | ID of a particular site            |
| species_id       | 2-letter code                      |
| sex              | sex of animal ("M", "F")           |
| hindfoot_length  | length of the hindfoot in mm       |
| weight           | weight of the animal in grams      |


## Challenge - DataFrames

Using our DataFrame `surveys_df`, try out the attributes & methods below to see
what they return.

1. `surveys_df.columns`
2. `surveys_df.shape` Take note of the output of `shape` - what format does it
return the shape of the DataFrame in?
3. `surveys_df.head()` Also, what does `surveys_df.head(15)` do?
4. `surveys_df.tail()`

## Challenge - Statistics

1. Create a list of unique site ID's ("plot_id") found in the surveys data. Call it
`site_names`. How many unique sites are there in the data? How many unique
species are in the data?

2. What is the difference between `len(site_names)` and `surveys_df['plot_id'].nunique()`?

## Challenge - Summary Data

1. How many recorded individuals are female `F` and how many male `M`?
2. What happens when you group by two columns using the following syntax and
   then calculate mean values?
   - `grouped_data2 = surveys_df.groupby(['plot_id', 'sex'])`
   - `grouped_data2.mean()`
3. Summarize weight values for each site in your data. HINT: you can use the
   following syntax to only create summary statistics for one column in your data.
   `by_site['weight'].describe()`

## Challenge - Make a list

What's another way to create a list of species and associated `count` of the
records in the data? *Hint:* you can perform `count`, `min`, etc. functions on
groupby DataFrames in the same way you can perform them on regular DataFrames.

## Challenge - Plots

1. Create a plot of average weight across all species per site.
2. Create a plot of total males versus total females for the entire dataset.

