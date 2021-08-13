# Link Fluentd to Elastic Search
1. Install Elastic Search Plugin to Fluentd
```
$> fluent-gem install fluent-plugin-elasticsearch
```
2. Change /etc/td-agent/td-agent.conf like following file
```
<match debug.**>
  @type elasticsearch
  host localhost
  port 9200
  index_name fluentd
</match>

<source>
  @type http
  @id input_http
  port 8888
</source>
```
3. Start Elastic Search service
```
$> brew services start elastic/tap/elasticsearch-full
```
4. Restart Fluentd service
```
$> sudo launchctl unload /Library/LaunchDaemons/td-agent.plist
$> sudo launchctl load /Library/LaunchDaemons/td-agent.plist
```
5. Add test data to Fluentd service
```
$> curl -X POST -d 'json={"json":"messi"}' http://localhost:8888/debug.test
```
6. Start Kibana service
```
$> brew services start elastic/tap/kibana-full
```
7. Open Kibana from Web browser
```
http://localhost:5601/
```
8. Search for Index Patterns
```
http://localhost:5601/app/management/kibana/indexPatterns
```
9. In index patterns, Search for
```
fluentd
```
10. Create the fluentd index pattern
11. Go to Discover
```
http://localhost:5601/app/discover
```
12. Change Index Pattern to
```
fluentd
```
