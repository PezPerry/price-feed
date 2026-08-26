# price-feed

Static price-serving JSON for the Equity & Markets Insight website, published
3-4x each weekday by the MasterControl price feed
(`C:\MasterControl\pricefeed\publish.ps1` on Mickey's PC).

Files: `manifest.json` (freshness probe), `latest.json` (all instruments,
one fetch), `anchors.json` (IRR window anchors + flags), `instruments.json`
(picker universe). Numbers are in as-quoted units; see `exponents` in
latest.json for minor/major-unit conversion. Keys are `TIDM:CCY` (or
`TIDM:CCY:DISAMBIGUATOR` for shared-ticker collisions).

This repo's history is disposable - the SQLite database and gzipped CSV archive
on the source machine are the durable record. History may be reset annually.
