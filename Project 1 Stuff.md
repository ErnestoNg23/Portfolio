#Visualisation of data using Seaborn

What the title says

```
sns.displot(data=df, x='rt_ms', stat='probability', hue='flankers', col='simon', alpha = .4, kind='hist', palette='bright')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142727936-d67f9de6-326f-4667-be84-a3c1cbf65300.png)


```
sns.displot(data=df, x='rt_clean', stat='probability', hue='flankers', col='simon', alpha = .4, kind='hist', palette='bright')
plt.show()
```
![image](https://user-images.githubusercontent.com/81998900/142727941-7ac266e0-6b58-4f26-93fe-017f8ba75aa8.png)
