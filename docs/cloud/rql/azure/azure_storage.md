---
id: azure_storage
title: Azure Storage
sidebar_label: Azure Storage
description: Azure Storage
---

# Sample RQL Queries

:::note
The following guide will walk you through Azure Storage RQL Query Examples
:::

## Azure Storage Not Geo-Redundant
:::note
The storage is not Geo-redundant. Your data is not durable in the case of a complete regional outage or a disaster in which the primary region is not recoverable
:::
```bash
config where cloud.type = 'azure' AND api.name = 'azure-storage-account-list' AND json.rule = properties.secondaryLocation does not exist
```