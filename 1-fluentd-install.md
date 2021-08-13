# Fluentd Installation
1. Install Fluentd on Mac with HomeBrew
```
$> brew install --cask td-agent
```
2.Start Fluentd
```
$> sudo launchctl load /Library/LaunchDaemons/td-agent.plist
```
3.See Fluentd process
```
$> sudo launchctl list | grep td-agent
```
4. See Fluentd log
```
$> tail -f /var/log/td-agent/td-agent.log
```
6. Send test data to Fluentd
```
$> curl -X POST -d 'json={"json":"message"}' http://localhost:8888/debug.test
```
7. Stop Fluentd process
```
$> sudo launchctl unload /Library/LaunchDaemons/td-agent.plist
```

# Fluentd Configuration Path
```
/etc/td-agent/td-agent.conf 
```
