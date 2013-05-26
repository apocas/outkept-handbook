<hr>
## Crawlers
You don't need to specify which servers and what do they support, `Outkept` will find this information for you.

This is what the crawlers do, they crawl the subnets you specified in `config.js` looking for machines that allow SSH connections using the ssh key you specified.

If `Outkept` finds a machine, it will look for a few properties (hostname, etc) about the machine and then it will look which sensors the machine supports by running the `verifier` command of each sensor.

<hr>
## Processes

Currently there are two main processes: one for server monitorization, control and crawling. Another for dashboard connections and data dispatching.

In a near future the number of processes will be increased, initially one dedicated for crawling and then servers control distributed across multiple processes.

<hr>
## SSH Connections

Each server has a SSH connection to it, inside this connection `Outkept` will use multiple channels in order to acquire it's sensor's data.

By default the majority of SSH daemons support 10 channels per connection, this does NOT mean that `Outkept` will only support 10 sensors for each server, instead `Outkept` implements a channel pool for each connection. This pool will consume commands from a queue.

If you set all your sensors in the millisecond range and your network's latency is high, your server queue up since the channel pool will not be able to dispatch it in time. When this happens a `queued` alert is shown in the dashboard in the affected server. To avoid this ajust sensors accordingly or increase the channel limit in your SSH daemon.

[meta:title]: <> (Architecture)
