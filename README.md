# flink-table-store-101 [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) [![Docker](https://badgen.net/badge/icon/docker?icon=docker&label)](https://https://docker.com/) [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

A playground for [Flink Table Store](https://github.com/apache/flink-table-store) (*abbr.* **FTS**) with multiple use cases and performance features.

*Read this in other languages* [简体中文](https://github.com/Myasuka/flink-table-store-101/blob/apple-silicon/README.zh.md)

## Use Cases
<table>
    <thead>
        <tr>
            <th>Demo</th>
            <th>Stack-involved Beyond FTS</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
          <td><b><code><a href="https://github.com/Myasuka/flink-table-store-101/tree/apple-silicon/real-time-update">Real-time Full and Incremental Snapshot Loading - Flink Table Store as a Streaming Lakehouse</a></code></b></td>
            <td rowspan=1>MySQL, Flink, Flink CDC</td>
            <td rowspan=2>Building streaming ETL pipelines for business analytics based on <a href="https://www.tpc.org/tpch/">TPC-H dataset</a></td>
        </tr>
        <tr>
          <td><b><code><a href="https://github.com/Myasuka/flink-table-store-101/tree/apple-silicon/lookup-join/README.md">Lookup Join and Pre-aggregated Insert using Flink Table Store</a></code></b></td>
          <td>MySQL, Flink, Flink CDC, Zeppelin</td>
        </tr>
    </tbody>
</table>

## Environment Prerequiste
- [Docker and Docker Compose](https://docs.docker.com/)

## Notes
Do not run demos simultaneously, there might be port conflicts.