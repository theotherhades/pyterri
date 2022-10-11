# pyterri
A simple python package for getting [territorial.io](https://territorial.io) player and clan data

*Still in early development*

## Installing
`pip install pyterri`

## Usage
Data for each clan is returned as a dictionary, with all values as strings
```py
{
   "clan": "ELITE",
   "rank": "5", 
   "score": "5.627"
}
```

When you get data for multiple clans at once, the individual dictionaries are returned inside a list, ordered based on rank
```py
[
    {
        "clan": "DREW",
        "rank": "1",
        "score": "14.238"
    },
    {
        "clan": "VOID",
        "rank": "2",
        "score": "11.734"
    },
    {
        "clan": "OG",
        "rank": "3",
        "score": "9.629"
    }
]
```

Get data for every currently listed clan
```py
from pyterri import clan
clan.getClans()
```

Get data for every clan up to a certain leaderboard position
```py
from pyterri import clan
clan.getClans(limit = 10) # Gets the top 10 clans
```

Get data for a clan from its tag
```py
from pyterri import clan
clan.getClan("ELITE")
```