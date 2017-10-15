[![wercker status](https://app.wercker.com/status/59e3bf8a0b4ddd0100557bd2/s/master "wercker status")](https://app.wercker.com/project/byKey/59e3bf8a0b4ddd0100557bd2)[![Go Report Card](https://goreportcard.com/badge/github.com/akhenakh/oureadb)](https://goreportcard.com/report/github.com/akhenakh/oureadb)  [![GoDoc](https://godoc.org/github.com/akhenakh/oureadb/index?status.svg)](https://godoc.org/github.com/akhenakh/oureadb/index)

## OureaDB

A general purpose geo data storing and indexing tool.

GeoJSON can be geo indexed and stored in protobuf (see `TestGeoJSONFeatureToGeoData()`) into different KV storages.

- Using badger database
- GoLevelDB
- BoltDB
- In memory using gtreap

Fast Geo & time Indexes are provided:

- `S2FlatIdx` a points, lines & polygons indexer, flat cover using s2

- `S2FlatTimeIdx` a geo reverse timed points, lines & polygons indexer, flat cover using s2

- `S2PointIdx` a point only generic indexer using s2

Debug tools:

- `S2CellQueryHandler()` returns a GeoJSON of cells tokens passed to it

- `GeoJSONToCellHandler()` returns a GeoJSON of cells covering the GeoJSON geometry passed to it