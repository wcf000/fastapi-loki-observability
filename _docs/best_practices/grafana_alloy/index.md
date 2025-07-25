Ingesting logs to Loki using Alloy

Grafana Alloy is a versatile observability collector that can ingest logs in various formats and send them to Loki. We recommend Alloy as the primary method for sending logs to Loki, as it provides a more robust and feature-rich solution for building a highly scalable and reliable observability pipeline.
Alloy flow diagram
Installing Alloy

To get started with Grafana Alloy and send logs to Loki, you need to install and configure Alloy. You can follow the Alloy documentation to install Alloy on your preferred platform.
Components of Alloy for logs

Alloy pipelines are built using components that perform specific functions. For logs these can be broken down into three categories:

    Collector: These components collect/receive logs from various sources. This can be scraping logs from a file, receiving logs over HTTP, gRPC or ingesting logs from a message queue.
    Transformer: These components can be used to manipulate logs before they are sent to a writer. This can be used to add additional metadata, filter logs, or batch logs before sending them to a writer.
    Writer: These components send logs to the desired destination. Our documentation will focus on sending logs to Loki, but Alloy supports sending logs to various destinations.

Log components in Alloy

Here is a non-exhaustive list of components that can be used to build a log pipeline in Alloy. For a complete list of components, refer to the components list.
Type Component
Collector loki.source.api
Collector loki.source.awsfirehose
Collector loki.source.azure_event_hubs
Collector loki.source.cloudflare
Collector loki.source.docker
Collector loki.source.file
Collector loki.source.gcplog
Collector loki.source.gelf
Collector loki.source.heroku
Collector loki.source.journal
Collector loki.source.kafka
Collector loki.source.kubernetes
Collector loki.source.kubernetes_events
Collector loki.source.podlogs
Collector loki.source.syslog
Collector loki.source.windowsevent
Collector otelcol.receiver.loki
Transformer loki.relabel
Transformer loki.process
Writer loki.write
Writer otelcol.exporter.loki
Interactive Tutorials

To learn more about how to configure Alloy to send logs to Loki within different scenarios, follow these interactive tutorials:

    Sending OpenTelemetry logs to Loki using Alloy
    Sending logs over Kafka to Loki using Alloy
