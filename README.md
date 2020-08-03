# metrics repo

Regularly collect and log metrics about IPFS related projects.

This repo contains a scheduled GitHub Action which pulls IPFS dependency data out of BigQuery and stores it 
in [timestamped json](./logs) files in this repo.

## Recent Data

### Google Trends

We're collecting the "interest over time" metric from Google Trends. From Google *"Numbers 
represent search interest relative to the highest point on the chart for the given region and 
time. A value of 100 is the peak popularity for the term. A value of 50 means that the term is 
half as popular. Likewise a score of 0 means the term was less than 1% as popular as the peak."*

This is the google trend data for searches of the term "IPFS" for the
last 12 months. The last 10 years is [available here.](./results/google-trends.md)



Google Trends:
*  7/2020: 64
*  6/2020: 67
*  5/2020: 63
*  4/2020: 68
*  3/2020: 57
*  2/2020: 60
*  1/2020: 61
*  12/2019: 54
*  11/2019: 58
*  10/2019: 63
*  9/2019: 59
*  8/2019: 67

### GitHub Search

These do a repository search, filtered by language, for "ipfs." This search
finds references to ipfs in project names, descriptions, and anything else
GitHub finds relevant (this isn't actually documented very well by GitHub).

GitHub limits the maximum results to 1K. We can get around this a little bit
by performing additional queries w/ different sorts in ascending and descending
order, but there's some amount we'll never get. That's why it's nice to have
the historical data logged in the repo every day.

The "total matches" we get is larger than the result set, even when the result
set is below the 1K limit imposed by GitHub. This isn't documented sufficiently
so we don't know why this is the case.

#### Go Repositories

Total Matches: 1755

Total Results (Limited by GitHUB API): 351

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [decentralized-identity/go-ipfs-ds-azure](https://github.com/decentralized-identity/go-ipfs-ds-azure)| 0 | 0 | 1| 2020-07-31 | 2020-07-31 |
| [wabarc/ipfs-pinner](https://github.com/wabarc/ipfs-pinner)| 0 | 0 | 17| 2020-07-18 | 2020-07-18 |
| [aschmahmann/ipfs-ds](https://github.com/aschmahmann/ipfs-ds)| 2 | 0 | 57| 2020-07-16 | 2020-07-16 |
| [diviramon/vbeam](https://github.com/diviramon/vbeam)| 3 | 1 | 196| 2020-07-06 | 2020-07-28 |
| [wabarc/wbipfs](https://github.com/wabarc/wbipfs)| 0 | 0 | 9682| 2020-07-04 | 2020-07-18 |
| [BDWare/go-ipfs](https://github.com/BDWare/go-ipfs)| 0 | 0 | 40531| 2020-07-01 | 2020-07-01 |
| [utkarsh23/access-control-for-IPFS](https://github.com/utkarsh23/access-control-for-IPFS)| 0 | 0 | 8| 2020-06-19 | 2020-06-19 |
| [StreamSpace/ss-ds-store](https://github.com/StreamSpace/ss-ds-store)| 1 | 0 | 17| 2020-06-13 | 2020-07-29 |
| [BasitAwan/IPFS-Crawler](https://github.com/BasitAwan/IPFS-Crawler)| 0 | 0 | 1675| 2020-06-10 | 2020-06-10 |
| [shiningacg/sn-ipfs](https://github.com/shiningacg/sn-ipfs)| 1 | 0 | 3881| 2020-06-04 | 2020-07-16 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 72850

Total Results (Limited by GitHUB API): 1322

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [GustaveNimant/irp_ipfs_full](https://github.com/GustaveNimant/irp_ipfs_full)| 0 | 0 | 56| 2020-08-02 | 2020-08-02 |
| [myst33d/IPFSUpload](https://github.com/myst33d/IPFSUpload)| 0 | 0 | 20| 2020-08-02 | 2020-08-02 |
| [rakaar/ipfs-logger](https://github.com/rakaar/ipfs-logger)| 0 | 0 | 88| 2020-08-01 | 2020-08-01 |
| [Permissionless-Software-Foundation/bch-w...](https://github.com/Permissionless-Software-Foundation/bch-wallet-plugin-postoffice)| 0 | 0 | 654| 2020-08-01 | 2020-08-01 |
| [devbootstrap/IPFS-vuejs-drizzle-app](https://github.com/devbootstrap/IPFS-vuejs-drizzle-app)| 0 | 0 | 130| 2020-07-29 | 2020-07-29 |
| [ARNiroula/test_ipfsnode](https://github.com/ARNiroula/test_ipfsnode)| 0 | 0 | 4628| 2020-07-28 | 2020-07-28 |
| [Sebastian-Gru/ipfs-prototype-spielereien](https://github.com/Sebastian-Gru/ipfs-prototype-spielereien)| 0 | 0 | 344| 2020-07-28 | 2020-07-29 |
| [Blockchain-DAV/BlockChainDAV](https://github.com/Blockchain-DAV/BlockChainDAV)| 0 | 0 | 163| 2020-07-28 | 2020-07-30 |
| [dhappy/cidcmp](https://github.com/dhappy/cidcmp)| 0 | 0 | 308| 2020-07-27 | 2020-07-31 |
| [shivasai780/Kyc-Blockchain-using-ipfs](https://github.com/shivasai780/Kyc-Blockchain-using-ipfs)| 0 | 0 | 42800| 2020-07-26 | 2020-07-26 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
