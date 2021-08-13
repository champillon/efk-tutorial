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
