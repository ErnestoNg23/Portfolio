# Visualisation using pandas .plot

Histograms! That is all.

```
df['rt_ms'].hist()
plt.axvline(df['rt_ms'].describe()['25%'], 0, 1, color='turquoise', linestyle='--')
plt.axvline(df['rt_ms'].median(), 0, 1, color='cyan', linestyle='-')
plt.axvline(df['rt_ms'].describe()['75%'], 0, 1, color='turquoise', linestyle='--')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142712926-f9f02e75-252f-434b-802e-7ee15f15a2a9.png)

```
plt.hist(df['rt_ms'], cumulative=True)
plt.axvline(df['rt_ms'].describe()['25%'], 0, 1, color='turquoise', linestyle='--')
plt.axvline(df['rt_ms'].median(), 0, 1, color='cyan', linestyle='-')
plt.axvline(df['rt_ms'].describe()['75%'], 0, 1, color='turquoise', linestyle='--')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142712935-af40999f-970a-415e-9fcb-72587c437dc0.png)
