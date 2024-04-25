Some of the functions available in the notebooks and codes in this repository
#understnanding the data
Load the dataset from the specified file path
dataset= pd.read_csv(file_path)

print(dataset.head(5)):Printing first 5 records of the dataset
dataset.shape:number of columns and row in the dataset
dataset.dtypes :data type of the dataset

#Exploratory Data Analysis (EDA) analysis
dataset.describe():Descriptive statistics for numerical variables
 Data Quality Check
 dataset.isnull().sum():Check for missing values
 #Time Series Analysis
 Plot the variables over time
plt.figure(figsize=(12, 8))
plt.subplot(2, 2, 1)
sns.lineplot(x='Timestamp', y='GHI', data=dataset)
plt.title('GHI over Time')
#Select relevant columns for temperature analysis
temperature_columns = ['TModA', 'TModB', 'Tamb']
dataset_temperatures = dataset[temperature_columns]
#Plot temperature distribution
plt.figure(figsize=(10, 6))
sns.boxplot(data=dataset_temperatures, orient='v')
plt.title('Temperature Distribution (Module and Ambient)')
plt.ylabel('Temperature (°C)')
plt.xticks(rotation=45)
plt.show()
Visualize the data: Create plots and charts (e.g., line plots, scatter plots, histograms, heatmaps)
Identify key trends: Look for trends or patterns in the data that indicate regions with high solar potential.
dataset_subset.corr():Perform statistical tests: Use appropriate statistical tests (e.g., correlation analysis, regression analysis) to quantify relationships between variables and assess the significance of findings.