#cyber/tool 

# Splunk

[Splunk Office Doc](https://docs.splunk.com/Documentation/Splunk/8.1.2/SearchTutorial/NavigatingSplunk)


Splunk is one of the leading SIEM solutions in the market. It allows users to collect, analyze, and correlate network and machine logs in real time.

- forwarder (collect data at endpoints and forward to splunk instance)
- indexer (parse and normalize data into field-value pair)
- search head (this is where analyst search/ using SPL splunk processing language)

Splunk lets you upload your own data files and run searches on them. Just like SQL, you can filter, sort, and analyze the data — but Splunk uses its own query language (SPL)
```
index=VPN_Logs Source_ip="107.3.206.58"
```