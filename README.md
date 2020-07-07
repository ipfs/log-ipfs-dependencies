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
*  7/2020: 71
*  6/2020: 69
*  5/2020: 73
*  4/2020: 69
*  3/2020: 61
*  2/2020: 60
*  1/2020: 56
*  12/2019: 55
*  11/2019: 60
*  10/2019: 65
*  9/2019: 60
*  8/2019: 62

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

Total Matches: 1740

Total Results (Limited by GitHUB API): 348

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [wabarc/wbipfs](https://github.com/wabarc/wbipfs)| 0 | 0 | 9679| 2020-07-04 | 2020-07-05 |
| [utkarsh23/access-control-for-IPFS](https://github.com/utkarsh23/access-control-for-IPFS)| 0 | 0 | 8| 2020-06-19 | 2020-06-19 |
| [StreamSpace/ss-ds-store](https://github.com/StreamSpace/ss-ds-store)| 0 | 0 | 11| 2020-06-13 | 2020-06-13 |
| [BasitAwan/IPFS-Crawler](https://github.com/BasitAwan/IPFS-Crawler)| 0 | 0 | 1675| 2020-06-10 | 2020-06-10 |
| [shiningacg/ipfs-filestore](https://github.com/shiningacg/ipfs-filestore)| 0 | 0 | 3863| 2020-06-04 | 2020-06-14 |
| [storj-thirdparty/driver-ipfs](https://github.com/storj-thirdparty/driver-ipfs)| 0 | 0 | 545| 2020-06-01 | 2020-07-02 |
| [bonedaddy/flloyd-archiver](https://github.com/bonedaddy/flloyd-archiver)| 4 | 0 | 108| 2020-05-31 | 2020-06-04 |
| [vulcanize/eth-ipfs-state-validator](https://github.com/vulcanize/eth-ipfs-state-validator)| 1 | 0 | 75| 2020-05-30 | 2020-07-01 |
| [storj-thirdparty/connector-ipfs](https://github.com/storj-thirdparty/connector-ipfs)| 0 | 1 | 220| 2020-05-30 | 2020-07-02 |
| [boomlinde/ipfs-gopher](https://github.com/boomlinde/ipfs-gopher)| 9 | 0 | 9| 2020-05-30 | 2020-05-31 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 73522

Total Results (Limited by GitHUB API): 1316

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [Jshanks21/ipfs-sandbox](https://github.com/Jshanks21/ipfs-sandbox)| 0 | 0 | 0| 2020-07-07 | 2020-07-07 |
| [tjayrush/unchainedindex.io](https://github.com/tjayrush/unchainedindex.io)| 0 | 0 | 207| 2020-07-06 | 2020-07-06 |
| [Permissionless-Software-Foundation/bch-w...](https://github.com/Permissionless-Software-Foundation/bch-wallet-starter)| 0 | 0 | 7096| 2020-07-06 | 2020-07-06 |
| [Tirthendu619/DAPP](https://github.com/Tirthendu619/DAPP)| 0 | 0 | 708| 2020-07-06 | 2020-07-06 |
| [plemonopoulos/upload_images_ipfs](https://github.com/plemonopoulos/upload_images_ipfs)| 0 | 0 | 935| 2020-07-01 | 2020-07-01 |
| [VIkash2601/eth_ipfs_file_upload](https://github.com/VIkash2601/eth_ipfs_file_upload)| 0 | 0 | 465| 2020-06-27 | 2020-07-02 |
| [rafaelramalho19/ipfs-css-icons](https://github.com/rafaelramalho19/ipfs-css-icons)| 0 | 0 | 191| 2020-06-26 | 2020-06-26 |
| [marstech3/block-doc](https://github.com/marstech3/block-doc)| 0 | 0 | 1000| 2020-06-26 | 2020-07-05 |
| [Gozala/js-ipfs-lite-http-client](https://github.com/Gozala/js-ipfs-lite-http-client)| 0 | 0 | 12| 2020-06-25 | 2020-07-01 |
| [ipfs-africa/ipfs-africa.github.io](https://github.com/ipfs-africa/ipfs-africa.github.io)| 0 | 0 | 6922| 2020-06-23 | 2020-06-24 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
