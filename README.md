# Elk_Stack
Introduction

The Elastic Stack — formerly known as the ELK Stack — is a collection of open-source software produced by Elastic which allows you to search, analyze, and visualize logs generated from any source in any format, a practice known as centralized logging. Centralized logging can be very useful when attempting to identify problems with your servers or applications, as it allows you to search through all of your logs in a single place. It’s also useful because it allows you to identify issues that span multiple servers by correlating their logs during a specific time frame.

The Elastic Stack has four main components:

Elasticsearch: a distributed RESTful search engine which stores all of the collected data.
Logstash: the data processing component of the Elastic Stack which sends incoming data to Elasticsearch.

Kibana: a web interface for searching and visualizing logs.

Beats: lightweight, single-purpose data shippers that can send data from hundreds or thousands of machines to either Logstash or Elasticsearch.

Here you will install the Elastic Stack on a CentOS 7 server. You will learn how to install all of the components of the Elastic Stack — including Filebeat, a Beat used for forwarding and centralizing logs and files — and configure them to gather and visualize system logs. Additionally, because Kibana is normally only available on the localhost, you will use Nginx to proxy it so it will be accessible over a web browser. At the end of this tutorial, you will have Elasticsearch, Kibana and Logstash on a  server, referred to as the Elastic Stack server, and Filebeat to push logs on the remote server.

Note: When installing the Elastic Stack, you should use the same version across the entire stack. This tutorial uses  Elasticsearch 6.5.2, Kibana 6.5.2, Logstash 6.5.2, and Filebeat 6.5.2

