# jsCrawler
### Simple Javascript Website crawler

This is a very simple and basic crawler that I developed to index the Six-Six website. For every article it will fetch the title, date and author. This is done based on the class-name that wraps these values.

At this moment the crawler needs to manually be provided with all the urls it needs to index. 

## What is does
The script accepts an array of URLS and loops through all of them. It will fetch and output the title, date and author for every page in a table

Because the script doesn’t index the links of the articles you need to input the articles to be indexed yourself. However, you can collect these easily via the developer console in your browser.

1. Go to the Six-Six website and choose any news category
2. Open the developer console and enter the following commands:
2.1. Command 1: Define a new array to put the links in
```
$a = new Array()
```
2.2. Command 2: Add all the links of the website in the array
```
$('.article-content a').each(function(){$a.push($(this).attr('href'))})
```
2.3. Command 3: Copy the array onto your clipboard
```
copy(JSON.stringify($a))
```
3. Copy this array into the urls var in index.html
4. Open index.html and the crawler starts automatically

On the Six-Six website you need to click a lot op load more, you can easily do this with the following command:
```
$("#load-more-button").click()
```

## Requirements
None, just run in from your browser and open the developer console.
