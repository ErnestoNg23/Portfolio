```python
df.isna().sum()
```




    id                     0
    year                   0
    month                  0
    day                    0
    hour                   0
    minute                 0
    gender                 0
    age                    0
    handedness             0
    wait                   0
    block                  0
    trial                  0
    target_location        0
    target                 0
    flankers               0
    rt                     2
    response               2
    error                  2
    pre_target_response    0
    ITI_response           0
    target_on_error        0
    dtype: int64



## Data Cleaning

```python
df.dropna()
```

</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>id</th>
      <th>year</th>
      <th>month</th>
      <th>day</th>
      <th>hour</th>
      <th>minute</th>
      <th>gender</th>
      <th>age</th>
      <th>handedness</th>
      <th>wait</th>
      <th>block</th>
      <th>trial</th>
      <th>target_location</th>
      <th>target</th>
      <th>flankers</th>
      <th>rt</th>
      <th>response</th>
      <th>error</th>
      <th>pre_target_response</th>
      <th>ITI_response</th>
      <th>target_on_error</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>2015</td>
      <td>5</td>
      <td>25</td>
      <td>14</td>
      <td>36</td>
      <td>f</td>
      <td>21</td>
      <td>r</td>
      <td>12.269</td>
      <td>practice</td>
      <td>1</td>
      <td>left</td>
      <td>black</td>
      <td>incongruent</td>
      <td>0.722</td>
      <td>black</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2015</td>
      <td>5</td>
      <td>25</td>
      <td>14</td>
      <td>36</td>
      <td>f</td>
      <td>21</td>
      <td>r</td>
      <td>12.269</td>
      <td>practice</td>
      <td>2</td>
      <td>right</td>
      <td>black</td>
      <td>incongruent</td>
      <td>0.472</td>
      <td>black</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2015</td>
      <td>5</td>
      <td>25</td>
      <td>14</td>
      <td>36</td>
      <td>f</td>
      <td>21</td>
      <td>r</td>
      <td>12.269</td>
      <td>practice</td>
      <td>3</td>
      <td>up</td>
      <td>white</td>
      <td>incongruent</td>
      <td>0.412</td>
      <td>white</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>2015</td>
      <td>5</td>
      <td>25</td>
      <td>14</td>
      <td>36</td>
      <td>f</td>
      <td>21</td>
      <td>r</td>
      <td>12.269</td>
      <td>practice</td>
      <td>4</td>
      <td>up</td>
      <td>black</td>
      <td>congruent</td>
      <td>0.560</td>
      <td>black</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>2015</td>
      <td>5</td>
      <td>25</td>
      <td>14</td>
      <td>36</td>
      <td>f</td>
      <td>21</td>
      <td>r</td>
      <td>12.269</td>
      <td>practice</td>
      <td>5</td>
      <td>down</td>
      <td>black</td>
      <td>congruent</td>
      <td>0.496</td>
      <td>black</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>187</th>
      <td>3</td>
      <td>2015</td>
      <td>5</td>
      <td>28</td>
      <td>14</td>
      <td>9</td>
      <td>f</td>
      <td>50</td>
      <td>r</td>
      <td>6.539</td>
      <td>5</td>
      <td>28</td>
      <td>left</td>
      <td>white</td>
      <td>congruent</td>
      <td>0.462</td>
      <td>white</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.023</td>
    </tr>
    <tr>
      <th>188</th>
      <td>3</td>
      <td>2015</td>
      <td>5</td>
      <td>28</td>
      <td>14</td>
      <td>9</td>
      <td>f</td>
      <td>50</td>
      <td>r</td>
      <td>6.539</td>
      <td>5</td>
      <td>29</td>
      <td>right</td>
      <td>white</td>
      <td>congruent</td>
      <td>0.353</td>
      <td>white</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>189</th>
      <td>3</td>
      <td>2015</td>
      <td>5</td>
      <td>28</td>
      <td>14</td>
      <td>9</td>
      <td>f</td>
      <td>50</td>
      <td>r</td>
      <td>6.539</td>
      <td>5</td>
      <td>30</td>
      <td>up</td>
      <td>black</td>
      <td>incongruent</td>
      <td>0.380</td>
      <td>white</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
    <tr>
      <th>190</th>
      <td>3</td>
      <td>2015</td>
      <td>5</td>
      <td>28</td>
      <td>14</td>
      <td>9</td>
      <td>f</td>
      <td>50</td>
      <td>r</td>
      <td>6.539</td>
      <td>5</td>
      <td>31</td>
      <td>left</td>
      <td>white</td>
      <td>neutral</td>
      <td>0.517</td>
      <td>white</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.023</td>
    </tr>
    <tr>
      <th>191</th>
      <td>3</td>
      <td>2015</td>
      <td>5</td>
      <td>28</td>
      <td>14</td>
      <td>9</td>
      <td>f</td>
      <td>50</td>
      <td>r</td>
      <td>6.539</td>
      <td>5</td>
      <td>32</td>
      <td>right</td>
      <td>black</td>
      <td>neutral</td>
      <td>0.444</td>
      <td>black</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>0.024</td>
    </tr>
  </tbody>
</table>
<p>574 rows × 21 columns</p>
</div>
