cluster-ops.md

# Cluster Operations

## Cluster Health
```
es_query: /_cluster/health
```

## Node Stats
```
es_query: /_cat/nodes?format=json&h=name,cpu,heap.percent,disk.used_percent
```

## List Indices
```
es_query: /_cat/indices/ppac*?format=json&s=index&h=index,health,status,docs.count,store.size
```

## Index Mapping
```
es_query: /<index>/_mapping
```

## ILM Policy
```
es_query: /_ilm/policy
```

## Shard Allocation
```
es_query: /_cat/shards/<pattern>?format=json&h=index,shard,prirep,state,docs,store,node
```

## Ingest Pipelines
```
es_query: /_ingest/pipeline
```
