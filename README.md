# LolCrawler
Crawls League of Legends match histories and match data and stores the data


## What it does
1. Start with the seed summoner as defined in config.py
2. Download match history of the chosen summoner and store it in MongoDB
3. Choose random match from the match history
4. Download match via API and store it in MongoDB
5. Choose random player from the downloaded match and continue with step 2

## Usage
Place your Riot API key in config.py. LolCrawler needs a region and a summoner id to start crawling. The config.py file provides a summoner seed for Europe West (EUW). You need to have MongoDB installed for storing the match and match history JSON files. 

Start crawling: 

```bash
python crawl.py 
```

Run the script in the background by using nohup: 
```bash
nohup python -u crawl.py &
```

Check if the script is still running with: 
```bash
ps ax | grep crawl.py
```

And kill LolCrawler by checking if the script is still running, checking the process id and then type:
```bash
kill <process-id>
```
## Changelog
### v0.2
Write to MongoDB, not to disk
### v0.1
Initial release

## Disclaimer
LolCrawler isn’t endorsed by Riot Games and doesn’t reflect the views or opinions of Riot Games or anyone officially involved in producing or managing League of Legends. League of Legends and Riot Games are trademarks or registered trademarks of Riot Games, Inc. League of Legends © Riot Games, Inc.



