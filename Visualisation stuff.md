# Visualisation using pandas .plot

Histograms are a valuable way of visualizing data in statistics, and it's a good thing that Python allows you to plot histograms. One way is through pandas using the .plot method. Reading from a dataframe, and in this case for reaction time in miliseconds (rt_ms), we're able to create a histogram of that dataset. Doing so allows us to visualize things, one of which is the distribution of the data. 

```
df['rt_ms'].hist()
plt.axvline(df['rt_ms'].describe()['25%'], 0, 1, color='turquoise', linestyle='--')
plt.axvline(df['rt_ms'].median(), 0, 1, color='cyan', linestyle='-')
plt.axvline(df['rt_ms'].describe()['75%'], 0, 1, color='turquoise', linestyle='--')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142712926-f9f02e75-252f-434b-802e-7ee15f15a2a9.png)

One cool thing that you can do that's one step beyond plotting a histogram is plotting a cumulative distribution function, which helps map out the cumulative distribution of a given variable. 

```
plt.hist(df['rt_ms'], cumulative=True)
plt.axvline(df['rt_ms'].describe()['25%'], 0, 1, color='turquoise', linestyle='--')
plt.axvline(df['rt_ms'].median(), 0, 1, color='cyan', linestyle='-')
plt.axvline(df['rt_ms'].describe()['75%'], 0, 1, color='turquoise', linestyle='--')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142712935-af40999f-970a-415e-9fcb-72587c437dc0.png)
