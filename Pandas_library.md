```python
                               ########READING DATA ########

import pandas as pd

print(pd.__version__)

df = pd.read_excel('/Users/dhanalakshmijothi/Desktop/python/GTEx/data/metadata/GTEx_Analysis_v8_Annotations_SubjectPhenotypesDD.xlsx')

df

```

    2.2.3





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>VARNAME</th>
      <th>VARDESC</th>
      <th>DOCFILE</th>
      <th>TYPE</th>
      <th>UNITS</th>
      <th>COMMENT1</th>
      <th>COMMENT2</th>
      <th>VALUES</th>
      <th>Unnamed: 8</th>
      <th>Unnamed: 9</th>
      <th>Unnamed: 10</th>
      <th>Unnamed: 11</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>SUBJID</td>
      <td>Subject ID, GTEx Public Donor ID</td>
      <td>NaN</td>
      <td>string</td>
      <td>NaN</td>
      <td>Subject ID, GTEx Public Donor ID</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AGE</td>
      <td>Age</td>
      <td>Demography</td>
      <td>integer</td>
      <td>Years</td>
      <td>Age</td>
      <td>Elapsed time since birth in years.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>SEX</td>
      <td>Sex</td>
      <td>Demography</td>
      <td>integer, encoded value</td>
      <td>NaN</td>
      <td>Sex</td>
      <td>The Donor's Identification of sex based upon s...</td>
      <td>1=Male</td>
      <td>2=Female</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>DTHHRDY</td>
      <td>Hardy Scale</td>
      <td>Death Circumstances</td>
      <td>integer, encoded value</td>
      <td>NaN</td>
      <td>Death Classification: 4-point Hardy Scale</td>
      <td>Death classification based on the 4-point Hard...</td>
      <td>0=Ventilator Case</td>
      <td>1=Violent and fast death</td>
      <td>2=Fast death of natural causes</td>
      <td>3=Intermediate death</td>
      <td>4=Slow death</td>
    </tr>
  </tbody>
</table>
</div>




```python
                               ######## CLEANING DATA  ########

df.fillna("", inplace = True)

df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>VARNAME</th>
      <th>VARDESC</th>
      <th>DOCFILE</th>
      <th>TYPE</th>
      <th>UNITS</th>
      <th>COMMENT1</th>
      <th>COMMENT2</th>
      <th>VALUES</th>
      <th>Unnamed: 8</th>
      <th>Unnamed: 9</th>
      <th>Unnamed: 10</th>
      <th>Unnamed: 11</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>SUBJID</td>
      <td>Subject ID, GTEx Public Donor ID</td>
      <td></td>
      <td>string</td>
      <td></td>
      <td>Subject ID, GTEx Public Donor ID</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1</th>
      <td>AGE</td>
      <td>Age</td>
      <td>Demography</td>
      <td>integer</td>
      <td>Years</td>
      <td>Age</td>
      <td>Elapsed time since birth in years.</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>2</th>
      <td>SEX</td>
      <td>Sex</td>
      <td>Demography</td>
      <td>integer, encoded value</td>
      <td></td>
      <td>Sex</td>
      <td>The Donor's Identification of sex based upon s...</td>
      <td>1=Male</td>
      <td>2=Female</td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>3</th>
      <td>DTHHRDY</td>
      <td>Hardy Scale</td>
      <td>Death Circumstances</td>
      <td>integer, encoded value</td>
      <td></td>
      <td>Death Classification: 4-point Hardy Scale</td>
      <td>Death classification based on the 4-point Hard...</td>
      <td>0=Ventilator Case</td>
      <td>1=Violent and fast death</td>
      <td>2=Fast death of natural causes</td>
      <td>3=Intermediate death</td>
      <td>4=Slow death</td>
    </tr>
  </tbody>
</table>
</div>


