Chrome extension displaying a wordcloud from news items matching
a given filter.

Created at the Newsreader hackathon:
http://www.newsreader-project.eu/hackathon/

Team members: Kaushik Chaubal, Manoj Nathwani, Derek Jones


The database searched is the Motor industry database built by the Newsreader
project: http://www.newsreader-project.eu/

The call used to obtain the data is:

https://newsreader.scraperwiki.com/actors_of_a_type?uris.0=dbo:Company&filter=highlighted_phrase&output=json

where: "highlighted_phrase" is extracted from the text highlighted, on a web page,
by the user.

Format of the json returned by api call from:

{

    "count": 1,  // number of pages available

    "payload" [ // The data we are interested in

        "comment": { } // Data to feed into the word cloud

             ]

}

There is a count field, but this is nto of any use since it applies
to all of the returned data, ie, the weight given to all fo it is
increase by the same amount.


When there is no data matching the query the json returned is:

{"error": "Result empty, possibly as a result of paging beyond results"}

