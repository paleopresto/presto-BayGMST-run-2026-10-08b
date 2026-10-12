# PReSto BayGMST run, 2026-10-08b pool (screened)

This repository runs the PReSto BayGMST reconstruction on a pinned LiPDverse data
pool. Everything that defines the run is committed here:

- `query_params.json` (`mode: bundle`): the pool bundle's URL and sha256,
  and its TSids. Pool `pages2k2017_localfdr10`: the PAGES 2k (2017) pool screened against local
  HadCRUT5 temperature (AR(1)-adjusted p, 10% false-discovery rate, 1850-2000),
  without series whose lag-1 autocorrelation exceeds 0.98. Pool, criteria, screen and deduplication:
  [paleopresto/presto-recipes](https://github.com/paleopresto/presto-recipes/tree/pools/pools),
  release [pools-2026-10-08b-r3](https://github.com/paleopresto/presto-recipes/releases/tag/pools-2026-10-08b-r3).
- The algorithm's config, from presto-recipes `runs/presto-BayGMST/2026-10-08b/`
  (or the template default where that directory has none).
- The workflow and container code, from the template's `pool-bundles` branch
  until that is merged upstream.

Committing `query_params.json` triggers the reconstruction workflow.
