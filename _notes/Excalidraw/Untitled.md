```python
# Create the years and durations lists
years = [2011,2012,2013,2014,2015,2016,2017,2018,2019,2020]
durations = [103, 101, 99, 100, 100, 95, 95, 96, 93,90]

# Create a dictionary with the two lists
movie_dict = dict(zip(years,durations))

# Print the dictionary
movie_dict
```


### Filtering a data frame in python
```python
# Subset the DataFrame for type "Movie"
netflix_df_movies_only = netflix_df.loc[netflix_df['type']=='Movie']

# Select only the columns of interest
netflix_movies_col_subset = netflix_df_movies_only.loc[:,['title','country','genre','release_year','duration']]

# Print the first five rows of the new DataFrame
print(netflix_movies_col_subset.head(5))
```


### Displaying a scatter plot in python
```python
# Create a figure and increase the figure size
fig = plt.figure(figsize=(12,8))

# Create a scatter plot of duration versus year
plt.scatter(netflix_movies_col_subset['release_year'],netflix_movies_col_subset['duration'])

# Create a title
plt.title("Movie Duration by Year of Release")
# Show the plot
plt.show()
```