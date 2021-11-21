# Visualisation of data using Seaborn

The Seaborn package for Python is an especially useful package for dealing with visualisation of data as well as for exploratory data analysis. While we have already explored how to visualize data using pandas, the Seaborn package is another tool in our data visualisation arsenal. 

First up is the code on how to plot a histogram using Seaborn, with a different color bin for each condition. 

```
sns.displot(data=df, x='rt_ms', stat='probability', hue='flankers', col='simon', alpha = .4, kind='hist', palette='bright')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142727936-d67f9de6-326f-4667-be84-a3c1cbf65300.png)

You'll notice that in the histogram above, something seems a little off. Bad code from a horrible programmer? Likely. Outliers? Likely too. We can clean up the data set that feeds the histogram and run it to see how it looks like!

```
sns.displot(data=df, x='rt_clean', stat='probability', hue='flankers', col='simon', alpha = .4, kind='hist', palette='bright')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142727941-7ac266e0-6b58-4f26-93fe-017f8ba75aa8.png)
