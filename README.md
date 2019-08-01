### box
---
https://github.com/cdgriffith/Box


```py
from box import Box
movie_data = {
  "Spaceballs": {
    "imdb stars": 7.1,
    "rating": "PG",
    "length": 96,
    "director": "Mel Brooks",
    "stars": [{"name": "Mel Brooks", "imdb": "nm0000316", "role": "President Skroob"},
      {"name": "John Candy", "imdb": "nm0001006", "role": "Barf"},
      {"name": "Rick Morais", "imdb": "nm0001548", "role": "Dark Helmet"}]
  },
  "Robin Hood: Men in Tights": {
    "imdb stars": 6.7,
    "rating": "PG-13",
    "length": 104,
    "director": "Mel Brooks",
    "stars": [
      {"name": "Cary Elwes", "imdb": "nm0000144", "role": "Robin Hood"},
      {"name": "Richard Lewis", "imdb": "nm0507659", "role": "Prince John"},
      {"name": "Roger Rees", "imdb": "nm0715953", "role": "Sheriff of Rottinggham"},
      {"name": "Amy Yasbeck", "imdb": "nm0001865", "role": "Marian"}
    ]
  }
}
movie_box = Box(movie_data)
movie_box.Robin_Hood_Men_inTights.imdb_stars
movie_box.movies.Spaceballs.stars[0].name
movie_box.movies.Spaceballs.stars.append({"name": "Bill Pullman", "imdb": "nm9999597", "role": "Lone Starr"})
movie_box.movies.Spaceballs.stars[-1].role


import requests
from box import BoxObject

def get_html(session, url, *args, **kwargs)
  response = session.get(url, *args, **kwargs)
  text = response.text
  response_meta = response.__dict__
  for key in tuple(filter(lambda k: k.startswitch('_'), response_meta)):
    response_meta.pop(key)
  return BoxObject(text, response_meta, frozen_box=True)
box_url = 'https://raw.githubusercontent.com/cdgriffitch/Box/master/box.py'
with requests.Session() as session:
  box_source = get_html(session, box_url)
box_source.url
box_source.status_code
box_source.raw.reason
```

```sh
pip install python-box
```

