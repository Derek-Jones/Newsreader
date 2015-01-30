Chrome extension generating wordcloud from news items matching
a given filter.

The database searched is the Motor industry database used by the Newsreader
project (http://www.newsreader-project.eu/)

The call used to obtain the data is:

https://newsreader.scraperwiki.com/actors_of_a_type?uris.0=dbo:Company&filter=highlighted_phrase&output=json

where: "highlighted_phrase" comes from the text highlighted on a web page.

Format of json returned by api call from:

{

    "count": 1,  // number of pages available

    "payload" [ // The data we are interested in

        "comment": { } // Data to feed into the word cloud

        "count": // Count of ??? instances of this item ?

             ]

}

When there is no data matching the query the json returned is:

{"error": "Result empty, possibly as a result of paging beyond results"}

