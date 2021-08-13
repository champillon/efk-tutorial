# Elastic Search Installation
1. Add new tap to HomeBrew for elastic/tap
```
$> brew tap elastic/tap
```
2. Install Elastic Search with HomeBrew
```
$> brew install elastic/tap/elasticsearch-full
```
3. Start Elastic Search service
```
$> brew services start elastic/tap/elasticsearch-full
```
4. Test Elastic Search service
```
$> curl http://localhost:9200
```
5. Check Elastic Search service status
```
$> brew services list
```
6. Stop Elastic Search service
```
$> brew services stop elastic/tap/elasticsearch-full
```
# Configuration Path
1. Data:
```
/usr/local/var/lib/elasticsearch/elasticsearch_[Host_Name]/
```
2. Logs:
```
/usr/local/var/log/elasticsearch/elasticsearch_[Host_Name].log
```
3. Plugins:
```
/usr/local/var/elasticsearch/plugins/
```
4. Config:
```
/usr/local/etc/elasticsearch/
```
