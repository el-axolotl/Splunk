# Splunk
Labs I used to learn Splunk

## Universal Forwarder For Windows

### Important File Locations

- ouputs.conf: A default exists at `C:\Program Files\SplunkUniversalForwarder\etc\system\default` which shouldn't be altered. Instead edit `C:\Program Files\SplunkUniversalForwarder\etc\system\local\outputs.conf` instead.

- splunkd.log: A log about the splunk forwarder service. Located at `C:\Program Files\SplunkUniversalForwarder\var\log\splunk\splunkd.log`

### Splunk.exe Commands

A command to debug outputs

```cmd
splunk.exe btool outputs list --debug
```

A command to add a receiver. This will create your outputs.conf file if none exists at `C:\Program Files\SplunkUniversalForwarder\etc\system\local`. 

```cmd
splunk.exe add forward-server <splunk-instance-name>.splunkcloud.com:9997
```