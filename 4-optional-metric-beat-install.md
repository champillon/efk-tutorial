# (Optional) Metricbeat Installation
1. Install Metricbeat with HomeBrew
```
$> brew install elastic/tap/metricbeat-full
```
2. Start Metricbeat service
```
$> brew services start elastic/tap/metricbeat-full
```
3. Check Metricbeat result in Elastic Search (wait for a minute then check)
```
$> curl -X GET "localhost:9200/_cat/indices?v"
```
4. Check Metricbeat service status
```
$> brew services list
```
5. Stop Metricbeat service
```
$> brew services stop elastic/tap/metricbeat-full
```
