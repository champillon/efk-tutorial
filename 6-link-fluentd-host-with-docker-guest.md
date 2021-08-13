# Link Fluentd host with Docker guest
1. Create the fluentd configuration file name "in_docker.conf" with following:
```
<source>
  @type forward
  port 24224
  bind 0.0.0.0
</source>

<match *.*>
  @type stdout
</match>
```
2. Start fluentd service with following command:
```
fluentd -c in_docker.conf
```
3. Run docker with following command:
```
docker run --rm --log-driver=fluentd --log-opt tag="docker.{{.ID}}" --log-opt fluentd-address=[HOST-IP]:24224 ubuntu echo 'Hello Fluentd!'
```
4. 'Hello Fluentd!' will show on Fluentd Service Thread
