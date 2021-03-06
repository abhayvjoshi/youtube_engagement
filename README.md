## Code usage
Quickstart bash script:
[run_all_wrangling.sh](/wrangling/run_all_wrangling.sh)
Place data in the [videos_json](/data/videos_json) directory.
Run `run_all_wrangling.sh` to create formatted data

## Python packages version
All codes are developed and tested in Python 3.6, along with NumPy 1.13, matplotlib 2.1 and SciPy 0.19.

## Video Data Fields
Each line is a YouTube video in `json` format, an example is shown below.
```json
{
   "id": "pFMj8KL8nJA",
   "snippet": {
      "description": "For more on India's goods and services tax and the future of the economy under Prime Minister Narendra Modi, CCTV America\u2019s Rachelle Akuffo interviewed Peter Kohli, the chief investment officer at D-M-S Funds.",
      "title": "Peter Kohli on the importance of the goods and services tax",
      "channelId": "UCj7wKsOBhRD9Jy4yahkMRMw",
      "channelTitle": "CCTV America",
      "publishedAt": "2016-08-10T00:34:01.000Z",
      "categoryId": "25",
      "detectLang": "en"
   },
   "contentDetails": {
      "duration": "PT5M27S",
      "definition": "hd",
      "dimension": "2d",
      "caption": "false"
   },
   "topicDetails": {
      "topicIds": ["/m/0546cd"],
      "relevantTopicIds": ["/m/03rk0", "/m/0gfps3", "/m/0296q2", "/m/05qt0", "/m/0dgrhmk", "/m/09x0r", "/m/05qt0", "/m/098wr"]
   },
   "insights": {
      "startDate": "2016-08-10",
      "days": "0,1,2,3,4,5,6,7,8,10,11,14,15,16,17,18,19,23,26,29,30,44,45,62,69,114,118,122,149,154,159,160,182,188,189,199,204,226,253",
      "dailyView": "70,11,15,7,7,8,11,4,7,2,2,1,6,6,3,2,2,2,1,1,4,1,1,1,1,2,3,1,1,1,1,3,1,2,2,1,1,1,1",
      "totalView": "281",
      "dailyWatch": "171.966666667,22.35,42.95,24.6333333333,26.05,25.3833333333,34.25,9.63333333333,6.31666666667,0.7,7.13333333333,0.0333333333333,15.2333333333,16.7,2.2,0.116666666667,0.966666666667,1.1,5.43333333333,5.43333333333,10.7666666667,1.2,5.43333333333,1.8,5.43333333333,5.45,3.15,0.2,1.68333333333,0.733333333333,0.483333333333,3.21666666667,5.43333333333,0.383333333333,5.6,0.0666666666667,0.533333333333,5.43333333333,1.06666666667",
      "avgWatch": "2.3290628707",
      "dailyShare": "2,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0",
      "totalShare": "2",
      "dailySubscriber": "0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0",
      "totalSubscriber": "0"
   }
}
```
## Output Result
A text file in the [train] (/data/train) directory.
The format of the output file will be {'id', 'publish', 'duration', 'definition', 'category', 'channel', 'topics', 'view30', 'watch30', 'wp30', 're30', 'days', 'daily_view', 'daily_watch'}
The field [re30] is the relative engagement score calculated on 30 days period.


