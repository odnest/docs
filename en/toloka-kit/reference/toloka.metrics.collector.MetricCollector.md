# MetricCollector
`toloka.metrics.collector.MetricCollector` | [Source code](https://github.com/Toloka/toloka-kit/blob/v0.1.24/src/metrics/collector.py#L18)

```python
MetricCollector(
    self,
    metrics: List[BaseMetric],
    callback: Callable[[Dict[str, List[Tuple[Any, Any]]]], None]
)
```

Gather metrics


**Examples:**

How to gather metrics and sends it to zabbix:

```python
import toloka.client as toloka
from toloka.metrics import MetricCollector, Balance, AssignmentsInPool
toloka_client = toloka.TolokaClient(token, 'PRODUCTION')
def send_metric_to_zabbix(metric_dict):
    pass
collector = MetricCollector(
    [
        Balance(),
        AssignmentsInPool('12345678'),
    ],
    send_metric_to_zabbix,
)
bind_client(collector.metrics, toloka_client)
asyncio.run(collector.run())
```
## Methods Summary

| Method | Description |
| :------| :-----------|
[create_async_tasks](toloka.metrics.collector.MetricCollector.create_async_tasks.md)| None
[run](toloka.metrics.collector.MetricCollector.run.md)| Starts collecting metrics. And never stops.
