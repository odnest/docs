# fit
`crowdkit.aggregation.classification.dawid_skene.DawidSkene.fit`

```python
fit(self, data: DataFrame)
```

Fit the model through the EM-algorithm.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`data`|**DataFrame**|<p>Performers&#x27; labeling results. A pandas.DataFrame containing `task`, `performer` and `label` columns.</p>

* **Returns:**

  self.

* **Return type:**

  'DawidSkene'