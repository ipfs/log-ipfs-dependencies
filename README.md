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
*  4/2021: 94
*  3/2021: 88
*  2/2021: 65
*  1/2021: 84
*  12/2020: 54
*  11/2020: 48
*  10/2020: 66
*  9/2020: 60
*  8/2020: 64
*  7/2020: 58
*  6/2020: 72
*  5/2020: 66

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

Total Matches: 1970

Total Results (Limited by GitHUB API): 394

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [anirudha-bs/Distributed_storage_ipfs](https://github.com/anirudha-bs/Distributed_storage_ipfs)| 0 | 0 | 16| 2021-04-20 | 2021-04-24 |
| [sebastiendan/go-ipfs](https://github.com/sebastiendan/go-ipfs)| 0 | 0 | 61695| 2021-04-09 | 2021-04-22 |
| [ohmpatel1997/ipfs-ethereum](https://github.com/ohmpatel1997/ipfs-ethereum)| 0 | 0 | 204531| 2021-04-04 | 2021-04-05 |
| [ninedraft/ursa](https://github.com/ninedraft/ursa)| 0 | 0 | 8| 2021-04-01 | 2021-04-01 |
| [ismdeep/ipfs-alive-keeper](https://github.com/ismdeep/ipfs-alive-keeper)| 0 | 0 | 7| 2021-03-29 | 2021-04-17 |
| [jimmyaxod/ipfscrawl](https://github.com/jimmyaxod/ipfscrawl)| 2 | 0 | 136| 2021-03-17 | 2021-04-19 |
| [seunggin/toolsForIPFS](https://github.com/seunggin/toolsForIPFS)| 0 | 0 | 1| 2021-03-15 | 2021-03-15 |
| [dikshabagdi/ipfs-api](https://github.com/dikshabagdi/ipfs-api)| 0 | 1 | 6| 2021-03-07 | 2021-03-07 |
| [DeedleFake/sips](https://github.com/DeedleFake/sips)| 1 | 0 | 28| 2021-03-02 | 2021-04-07 |
| [paulgmiller/zebu](https://github.com/paulgmiller/zebu)| 0 | 0 | 79| 2021-03-01 | 2021-04-25 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 83330

Total Results (Limited by GitHUB API): 1459

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [luizoamorim/decentragram](https://github.com/luizoamorim/decentragram)| 0 | 0 | 488| 2021-04-25 | 2021-04-26 |
| [newlinedeveloper/Decentralized-storage](https://github.com/newlinedeveloper/Decentralized-storage)| 0 | 0 | 1245| 2021-04-25 | 2021-04-25 |
| [shaoye/ipfs-vault](https://github.com/shaoye/ipfs-vault)| 0 | 0 | 488| 2021-04-22 | 2021-04-25 |
| [imestin/ipfs-blog-website](https://github.com/imestin/ipfs-blog-website)| 0 | 0 | 5175| 2021-04-20 | 2021-04-21 |
| [nftstorage/ipfs-cluster](https://github.com/nftstorage/ipfs-cluster)| 7 | 0 | 398| 2021-04-20 | 2021-04-22 |
| [christroutner/ipfs-wss-peers](https://github.com/christroutner/ipfs-wss-peers)| 1 | 0 | 334| 2021-04-19 | 2021-04-21 |
| [imestin/ipfs-blog-uploader](https://github.com/imestin/ipfs-blog-uploader)| 0 | 0 | 29| 2021-04-19 | 2021-04-20 |
| [jthug/ipfs-nft](https://github.com/jthug/ipfs-nft)| 0 | 0 | 3659| 2021-04-19 | 2021-04-19 |
| [lucylow/medblock](https://github.com/lucylow/medblock)| 0 | 0 | 10565| 2021-04-17 | 2021-04-25 |
| [mohammadreza-ashouri/DDrive](https://github.com/mohammadreza-ashouri/DDrive)| 0 | 0 | 516| 2021-04-15 | 2021-04-15 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
