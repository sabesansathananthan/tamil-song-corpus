# tamil-song-corpus :notes:

[![GitHub repo size](https://img.shields.io/github/repo-size/sabesansathananthan/tamil-song-corpus?color=red&style=plastic)](https://github.com/sabesansathananthan/tamil-song-corpus)
[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/sabesansathananthan/tamil-song-corpus?style=plastic)](https://github.com/sabesansathananthan/tamil-song-corpus)
[![GitHub](https://img.shields.io/github/license/sabesansathananthan/tamil-song-corpus?color=orange&style=plastic)](https://github.com/sabesansathananthan/tamil-song-corpus/blob/master/LICENSE)
[![GitHub language count](https://img.shields.io/github/languages/count/sabesansathananthan/tamil-song-corpus?color=brightgreen&style=plastic)](https://github.com/sabesansathananthan/tamil-song-corpus)
[![GitHub top language](https://img.shields.io/github/languages/top/sabesansathananthan/tamil-song-corpus?color=blueviolet&style=plastic)](https://github.com/sabesansathananthan/tamil-song-corpus)
[![Twitter Follow](https://img.shields.io/twitter/follow/TheSabesan?color=lightgrey&style=plastic)](https://twitter.com/intent/follow?original_referer=https%3A%2F%2Fpublish.twitter.com%2F%3FbuttonType%3DFollowButton%26query%3Dhttps%253A%252F%252Ftwitter.com%252FTheSabesan%26widget%3DButton&ref_src=twsrc%5Etfw&screen_name=TheSabesan&tw_p=followbutton)

This repo contains 4216 songs data scraped from [Tamilpaa](https://www.tamilpaa.com) and stored at [`tamilpaa_data.txt`](/Data/tamilpaa_data.txt) file. All the metadata are in English. [`Web_scraping_tamilpaa.ipynb`](/Web_scraping_tamilpaa.ipynb) is used to scrap the data.

## JSON Structure

### JSON structure of scraped song

```JSON
"{'movie_name': '10 Enradhukulla (10 எண்றதுகுள்ள) ', 'year': '2015', 'music': 'D. Imman', 'actors': 'Vikram, Samantha', 'movie_url': 'https://www.tamilpaa.com/10-enradhukulla-songs-lyrics', 'movie_image': 'https://www.tamilpaa.com/upload/movies/10-enradhukulla.jpg', 'movie_name_tamil': '10 எண்றதுகுள்ள', 'movie_name_eng': '10 Enradhukulla', 'movie_song': [{'song_name': '\nVroom Vroom (\nபேர கேட்டா )', 'song_url': 'https://www.tamilpaa.com/3000-vroom-vroom-tamil-songs-lyrics', 'song_music': 'D. Imman', 'song_lyrics': 'Madhan Karky', 'song_singers': '', 'song_fulllyrics': 'பேர கேட்டா \xa0பேஜாரு பண்ற\nமெய்ய சொல்லு யாருடா\xa0நீ\nfees-u வாங்கி confuse-u பண்ற\nமெய்ய சொல்லு யாருடா \xa0நீ\n\nநான் பாஞ்ச bullet-u தான்\nஆபத்தே chicklet\xa0 தான்\nகார் ஓட்டும் fight jet-u நான்\nபொண்ணுங்க மாக்நெட்-உ நான்\nஎனக்குன்னு இல்ல கூண்டு\nஉன் நெஞ்சில ஏன்டா காண்டு\nஉனக்கென்ன வேணும் வேண்டு\nஎன்னோட பேரு \xa0bond-u\nBond James Bond\n\nபேர கேட்டா \xa0பேஜாரு பண்ற\nமெய்ய சொல்லு யாருடா\xa0நீ\nfees-u வாங்கி confuse-u பண்ற\nமெய்ய சொல்லு யாருடா \xa0நீ\n\nஎன் கண்ணில் அச்சம் இல்ல\nஎன் போல உச்சம் இல்ல\nஊருக்கு செல்ல புள்ள\nஎதிரிக்கி நான் தான் தொல்ல\nஎனக்குன்னு இல்ல வேலி\nநான் ஆடுற வரைக்கும் ஜாலி\nஅடிச்சா எல்லாரும் காலி\nஎன்னோட பேரு கொஹ்லி\nKohli Virat Kohli\n\nஎன் ஊரு பரமக்குடி\nநான் யாரு கண்டுபிடி\nமொத்த வித்த அத்துப்படி\nஎன் கிட்ட கத்துகடி\nபடிப்புக்கு போவல tuition\nஆனா நடிப்புல நான் ஒரு ocean\nபுதுமைகதான் என் பேஷன்\nஎன்னோட பேரு ஹாசன்\nHassan Kamal Hassam\n\nநீங்க நல்லவரா இல்ல கெட்டவரா \nரெண்டும் செந்ததுதான் நான்\ni am a hero and a villain'}]}"
```

Randomly selected 1500 songs data are fully translated to Tamil and extra metadata such as "song_lyrics", "song_music", "song_singers" are added to improve the quality of the search and stored as [`tamil_songs_corpus.txt`](/Data/tamil_songs_corpus.txt) file. [`pre_processing.ipynb`](/pre_processing.ipynb) is used to produce these JSON data.

### JSON structure of a processed song

```JSON
{ "index" : { "_index" : "songs_db_index", "_type" : "songs", "_id" :1 }}
{"movie_name": "அலைபாயுதே", "song_name": "யாரோ யாரோட", "song_music": "ஏ.ஆர்.ரஹ்மான்", "song_lyrics": "வைரமுத்து", "song_singers": "மஹாலட்சுமி ஐயர், வைஷாலி சமந்த், ரிச்சா சர்மா", "year": "2000", "actors": "ஆர் மாதவன், ஷாலினி", "song_rating": 5, "song_url": "https://www.tamilpaa.com/2553-yaro-yarodi-tamil-songs-lyrics", "song_fulllyrics": "யாரோ யாரோடி ஒன்னோட புருசன்\nயாரோ யாரோடி உன் திமிருக்கு அரசன்\nயாரோ யாரோடி ஒன்னோட புருசன்\nயாரோ யாரோடி உன் திமிருக்கு அரசன்\n\nஈக்கி போல லாவடிக்க இந்திரனார் பந்தடிக்க\nஅந்தப் பந்தை தீர்த்தடிப்பவனோ சொல்லு\nசந்தனப் பொட்டழகை சாஞ்ச நடையழகை\nவெளி வேட்டி கட்டியவனோ சொல்லு\n\nயாரோ யாரோடி ஒன்னோட புருசன்\nயாரோ யாரோடி உன் திமிருக்கு அரசன்\nயாரோ யாரோடி ஒன்னோட புருசன்\nயாரோ யாரோடி உன் திமிருக்கு அரசன்\n\nதங்கத்துக்கு வேர்க்குது பாருங்க பாருங்க\nசாந்து கண்ணும் மயங்குது ஏனுங்க ஆ\nமுத்தழகி இங்கே இல்லீங்க சொல்லுங்க\nமுத்தமிட்டு எங்கே தொடுங்க\nமொத்தமாக சொல்லிக் குடுங்க\nசொல்லிக் குடுங்க குடுங்க குடுங்க குடுங்க\nகன்னிப் பொண்ணு நல்லா நடிப்பா அவ நடிப்பா\nகட்டிலுக்குப் பாட்டுப் படிப்பா\n\nயாரோ யாரோடி ஒன்னோட புருசன்\nஆத்தி அவந்தாண்டி உன் திமிருக்கு அரசன்\nஈக்கி போல லாவடிக்க இந்திரனார் பந்தடிக்க\nஅந்தப் பந்தை தீர்த்தடிப்பவனோ சொல்லு\nமல்லு வேட்டி கட்டி வந்த சல்லிக்கட்டு மாட்ட முட்டி\nமல்லியப்பூ வெல்லப்போவுதடி நில்லு\n\n...\nகண்ணாலம் கண்ணாலம் பூங்கொடிக்குக் கண்ணாலம் பூங்கொடிக்குக் கண்ணாலம் (3)\nகண்ணாலம்...கண்ணாலம்...பூங்கொடிக்குக் கண்ணாலம்...பூங்கொடிக்குக் கண்ணாலம்\n\nபொன் தாலி பொண்ணுக்கெதுக்கு எதுக்கு\nமூணு முடி போடுவதெதுக்கு...ஆ\nஉரிமைக்காக ஒத்த முடிச்சு\nஉரிமைக்காக ஒத்த முடிச்சு அடியே\nஉறவுக்காக ரெண்டாம் முடிச்சு\nஊருக்காக மூணாம் முடிச்சு\nமுடிச்சு...முடிச்சு முடிச்சு முடிச்சு\nபொன் தாலி பொண்ணுக்கெதுக்கு எதுக்கு\nமூணு முடி போடுவதெதுக்கு\n\nயாரோ யாரோடி ஒன்னோட புருசன்\nயாரோ யாரோடி உன் திமிருக்கு அரசன்\nயாரோ யாரோடி ஒன்னோட புருசன்\nயாரோ யாரோடி உன் திமிருக்கு அரசன"}
```

Bulk API format of those 1500 songs are stored as [`tamil_songs_corpus_final.txt`](/Data/tamil_songs_corpus_final.txt) file.

> :memo: **NOTE**
>
> > #### **Attributes**
> >
> > - **movie_name**: Name of the movie featured in the song.
> > - **song_name**: Song Name in Tamil.
> > - **song_music**: Music director of the Song.
> > - **song_lyrics**: Song lyrics writer of the songs.
> > - **song_singers**: Comma Separated Song Singers of the songs.
> > - **year**: Year of Movie released.
> > - **actors**: Comma Separated Actors Names.
> > - **song_rating**: The rating of the song (Random value).
> > - **song_url**: Song URL in the TamilPaa website.
> > - **song_fulllyrics**: Full Lyrics of the Songs in Tamil.

## Instructions

1. Install Elasticsearch from the [website](https://www.elastic.co/downloads/) to localhost or web server.
2. Upload Bulk API format songs by run the [`iR.py`](/iR.py) file.

> :information_source: **TIP**
>
> > For detailed steps on installing elasticsearch and sample-site watch this [`video`](https://www.youtube.com/watch?v=BpLDDuCaOTA&t=81s)

## Query DSL for ElasticSearch search engine

- Deleting an index(database)

```JSON
DELETE /songs_db_index
```

> :exclamation: **IMPORTANT**
>
> > - The below code must be run before creating the index(database).
> > - Make a folder named analysis in elasticserach config folder.
> > - Please copy [`tamil_stopwords.txt`](/Data/tamil_stopwords.txt) & [`tamil_stemming.txt`](/Data/tamil_stemming.txt) to the analysis folder.

- Custom stop words and stemming new analyzer along with the standard analyzer

```JSON
PUT /songs_db_index/
{
       "settings": {
           "analysis": {
               "analyzer": {
                   "my_analyzer": {
                       "tokenizer": "standard",
                       "filter": ["custom_stopper","custom_stems"]
                   }
               },
               "filter": {
                   "custom_stopper": {
                       "type": "stop",
                       "stopwords_path": "analysis/tamil_stopwords.txt"
                   },
                   "custom_stems": {
                       "type": "stemmer_override",
                       "rules_path": "analysis/tamil_stemming.txt"
                   }
               }
           }
       }
   }
```

- Checking the custom analyzer(stopwords, stemming)

```JSON
GET /songs_db_index/_analyze
{
 "text": ["மிகவும் இனிமையான ஒரு 10 பாடல்கள்"],
 "analyzer": "my_analyzer"
}
```

- Using custom indexing for search. ஹரிஸ் ஜெயராஜ் songs spelling mistake

```JSON
GET /songs_db_index/songs/_search
{
   "query": {
       "multi_match" : {
           "query" : "ஹஷ்ரி ஜெராயஜ்",
           "fuzziness": "AUTO",
       "analyzer": "my_analyzer"
       }
   }
}
```

- Using standard indexing for search. ஹரிஸ் ஜெயராஜ் songs spelling mistake.

```JSON
GET /songs_db_index/songs/_search
{
   "query": {
       "multi_match" : {
           "query" : "ஹஷ்ரி ஜெராயஜ்",
           "fuzziness": "AUTO",
       "analyzer": "standard"
       }
   }
}
```

- Top 10 songs from 2010 to 2020 using `song_rating`

```JSON
GET /songs_db_index/songs/_search
{
   "size" : 10,
    "sort" : [
       { "song_rating" : {"order" : "desc"}}
   ],
   "query": {
       "range" : {
           "year" : {
               "gte" : "2010",
               "lte" :  "2020"
           }
       }
   }
}
```

- Top 10 songs from 2010 to 2020 filter output

```JSON
GET /songs_db_index/songs/_search
{
   "_source":["movie_name", "song_name" ],
   "size" : 10,
    "sort" : [
       { "song_rating" : {"order" : "desc"}}
   ],
   "query": {
       "range" : {
           "year" : {
               "gte" : "2010",
               "lte" :  "2020"
           }
       }
   }
}
```

- Top 10 songs from 2019

```JSON
GET /songs_db_index/songs/_search
{
   "size":10,
   "sort" : [
       { "song_rating" : {"order" : "desc"}}
   ],
   "query": {
       "multi_match": {
             "query" : "2019",
           "fields":["year"],
           "fuzziness": "AUTO"
       }
   }
}
```

<center><strong>- OR -</strong></center>

```JSON
GET /songs_db_index/songs/_search
{
   "size":10,
   "sort" : [
       { "song_rating" : {"order" : "desc"}}
   ],
   "query": {
       "match": {
           "year": {
           "query": "2019",
           "fuzziness": "AUTO"
           }
       }
   }
}
```

- Search by lyrics spelling mistake

```JSON
GET /songs_db_index/_search
{
 "query": {
   "multi_match" : {
     "query":    "வித்தை விதைத் காதல் வித்தை",
     "fuzziness": "AUTO"
   }
 }
}
```

- இளையராஜா songs boosting `song_singers` by 3

```JSON
GET /songs_db_index/_search
{
   "query": {
       "multi_match" : {
           "query" : "இளையராஜா",
           "fields": ["song_music", "song_singers^3"]
       }
   }
}
```

- யுவன் சங்கர் ராஜா 2019 songs

```JSON
GET /songs_db_index/_search
{
"query": {
  "bool": {
        "must": [
            { "match": { "song_music": "யுவன் சங்கர் ராஜா" }},
            { "match": { "year": "2019" }}
        ]
      }
    }

}
```

- ஏ.ஆர்.ரஹ்மான் latest songs using bool must

```JSON
GET /songs_db_index/_search
{
 "query": {
   "bool": {
     "must": [{
         "match": {
           "song_music": "ஏ.ஆர்.ரஹ்மான்"
         }
       },
       {
         "range": {
           "year" : {
               "gte" : "2015"
           }
         }
       }
     ]
   }
 }
}
```

- Latest songs, new songs

```JSON
GET /songs_db/_search
{
   "query": {
       "range": {
           "year" : {
               "gte" : "2019"
           }
       }
   }
}
```

- Songs which released after 2010 and `song_music` by யுவன் சங்கர் ராஜா but not sung by யுவன் சங்கர் ராஜா

```JSON
GET /songs_db_index/_search
{
 "query": {
   "bool": {
     "must": {
       "bool" : {
         "filter": [
       {
         "range": {
           "year" : {
               "gte" : "2010"
           }
         }
       }
     ],
         "must": { "match": { "song_music": "யுவன் சங்கர் ராஜா" }}
       }
     },
     "must_not": { "match": {"song_singers": "யுவன் சங்கர் ராஜா" }}
   }
 }
}
```

- `song_music` name ending in ன்

```JSON
GET /songs_db_index/_search
{
   "query": {
       "wildcard" : {
           "song_music" : "*ன்"
       }
   },
   "_source": ["song_music"],
   "highlight": {
       "fields" : {
           "song_music" : {}
       }
   }
}
```

- Top 10 ஏ.ஆர்.ரஹ்மான் பாடல்கள்

```JSON
GET /songs_db_index/_search
{
 "size":10,
   "sort" : [
       { "song_rating" : {"order" : "desc"}}
   ],
 "query": {
   "multi_match" : {
     "query":    "ஏ.ஆர்.ரஹ்மான்",
     "fields":["song_music"],
     "fuzziness": "AUTO"
   }
 }
}
```

- Search songs by movie

```JSON
GET /songs_db_index/_search
{
   "query": {
       "multi_match": {
           "fields":["movie_name"],
           "query" : "என்னை அறிந்தால்",
           "fuzziness": "AUTO"
       }
   }
}
```

- Term query for exact match

```JSON
GET /songs_db_index/_search
{
 "query": {
   "term": {
     "movie_name":"என்னை அறிந்தால்"
   }
 }
}
```

- For multiple indexes(databases) search

```JSON
GET /_all/_search
{
 "query": {
   "term": {
     "movie_name":"என்னை அறிந்தால்"
   }
 }
}
```
