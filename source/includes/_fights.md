# Fights

## Get a specific fight

```ruby
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
  "fight_id": "587add847b6df2262d40749c",
  "data": [
    {
      "event_id": "5861bafe0503c3eb32db94c0",
      "status": "finalizada",
      "order": 99,
      "rounds": 1,
      "round_active": 1,
      "main_event": true
    }
  ],
  "result": [
    {
      "winner": "winnerRed",
      "winner_by": "TKO",
      "at_round": "1",
      "at_time": "0:48"
    }
  ],
  "fighters": [
    {
      "red": [
        {
          "fighter_id": "56d4d1a19f0e9d0c09671960",
          "first_name": "Amanda",
          "last_name": "Nunes",
          "full_name": "Amanda Nunes",
          "nick_name": "The Lioness",
          "country": "br"
        }
      ],
      "blue": [
        {
          "fighter_id": "56410d10ec89eecc2b68f82e",
          "first_name": "Ronda",
          "last_name": "Rousey",
          "full_name": "Ronda Rousey",
          "nick_name": "Rowdy",
          "country": "us"
        }
      ]
    }
  ],
  "tale": [
    {
      "age": [
        {
          "info_name": "Age",
          "red": "28",
          "blue": "29"
        }
      ],
      "height": [
        {
          "info_name": "Height",
          "red": "5'5\"",
          "blue": "5'6\""
        }
      ],
      "reach": [
        {
          "info_name": "Reach",
          "red": "69.0\"",
          "blue": "66.0\""
        }
      ],
      "weight": [
        {
          "info_name": "Weight",
          "red": "135.0 lbs",
          "blue": "135.0 lbs"
        }
      ],
      "record": [
        {
          "info_name": "Record",
          "red": "13 / 0 / 4",
          "blue": "12 / 0 / 1"
        }
      ],
      "wins": [
        {
          "info_name": "Wins",
          "red": "13",
          "blue": "12"
        }
      ],
      "draws": [
        {
          "info_name": "Draws",
          "red": "0",
          "blue": "0"
        }
      ],
      "loses": [
        {
          "info_name": "Loses",
          "red": "4",
          "blue": "1"
        }
      ],
      "city": [
        {
          "info_name": "City",
          "red": "Bahia",
          "blue": "California"
        }
      ],
      "team": [
        {
          "info_name": "Team",
          "red": "ATT",
          "blue": "Glendale"
        }
      ],
      "style": [
        {
          "b": "Style",
          "red": "-",
          "blue": "Judo"
        }
      ]
    }
  ],
  "stats": [
    {
      "stats_name": "Strikes Thrown",
      "slug_name": "strikes-thrown",
      "rounds": [
        {
          "red": 48,
          "blue": 12
        }
      ]
    },
    {
      "stats_name": "Significant Strikes Landed",
      "slug_name": "significant-strikes-landed",
      "rounds": [
        {
          "red": 19,
          "blue": 1
        }
      ]
    },
    {
      "stats_name": "Takedowns Attempted",
      "slug_name": "takedowns-attempted",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Takedowns",
      "slug_name": "takedowns",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Submissions attempted",
      "slug_name": "submissions-attempted",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Takedowns Defended",
      "slug_name": "takedowns-defended",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Cage Control",
      "slug_name": "cage-control",
      "rounds": [
        {
          "red": "0",
          "blue": "0"
        }
      ]
    },
    {
      "stats_name": "Ground Control",
      "slug_name": "ground-control",
      "rounds": [
        {
          "red": "0",
          "blue": "0"
        }
      ]
    }
  ]
}
```


Para as lutas não temos um endpoint que retorne todas elas porque não faz muito sentido na minha opinião. Os filtros de lutas em views sempre serão a partir de algum lutador, ou a partir de alguem evento. O widget de luta é para análise ou comparação com outras de um mesmo lutador ou evento. 

O Json retornado é separado em 5 "áreas":
- `"data"` 
- `"result"` 
- `"fighters"` 
- `"tale"` 
- `"stats"`

Foi feito assim porque são os componentes básicos da view. Fica mais fácil de chamar eles nos loops separados pelas divs do layout.

Outra coisa também é que tanto em `stats` `tale` é um loop chato de fazer e chamar cada um dos stats, do jeito que foi feito é só fazer um loop que vai pegar todos e até os nomes.

## Parametros de data

```
"data": [
    {
      "event_id": "5861bafe0503c3eb32db94c0",
      "status": "finalizada",
      "order": 99,
      "rounds": 1,
      "round_active": 1,
      "main_event": true
    }
  ],
```

Data é o mais simples de todos, basicamente só strings que servem de informação para o evento, seguem abaixo:

Parameter | Type | Description
--------- | ------- | -----------
`event_id` | string | ...
`status` | string | ...
`order` | string | ...
`rounds` | string | ...
`round_active` | string | ...
`main_event` | boolean | ...

## Parametros de result
```
  "result": [
    {
      "winner": "winnerRed",
      "winner_by": "TKO",
      "at_round": "1",
      "at_time": "0:48"
    }
  ],
```
A parte de resultados

Parameter | Type | Description
--------- | ------- | -----------
`winner` | string | ...
`winner_by` | string | ...
`at_round` | string | ...
`at_time` | string | ...

## Parametros de fighters

Parameter | Type | Description
--------- | ------- | -----------
`fighters` | array | ...



```
  "fighters": [
    {
      "red": [
        {
          "fighter_id": "56d4d1a19f0e9d0c09671960",
          "first_name": "Amanda",
          "last_name": "Nunes",
          "full_name": "Amanda Nunes",
          "nick_name": "The Lioness",
          "country": "br"
        }
      ],
      "blue": [
        {
          "fighter_id": "56410d10ec89eecc2b68f82e",
          "first_name": "Ronda",
          "last_name": "Rousey",
          "full_name": "Ronda Rousey",
          "nick_name": "Rowdy",
          "country": "us"
        }
      ]
    }
  ],
```

## Array de tale


Parameter | Type | Description
--------- | ------- | -----------
`tale_name` | string | ...
`red` | string | ...
`blue` | string | ...


```ruby

  for item in @tale
  
    item["tale_name"] 
    item["red"]
    item["blue"]
  
  end

```

## Array de stats


```ruby

for round in rounds 
  i = 0
  for stat in @stats
  
    stat["stats_name"]
    stat["rounds"][i]["red"]
    stat["rounds"][i]["blue"]
  
  end
  i+
end

```

```
  "stats": [
    {
      "stats_name": "Strikes Thrown",
      "slug_name": "strikes-thrown",
      "rounds": [
        {
          "red": 48,
          "blue": 12
        }
      ]
    },
    {
      "stats_name": "Significant Strikes Landed",
      "slug_name": "significant-strikes-landed",
      "rounds": [
        {
          "red": 19,
          "blue": 1
        }
      ]
    },
    {
      "stats_name": "Takedowns Attempted",
      "slug_name": "takedowns-attempted",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Takedowns",
      "slug_name": "takedowns",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Submissions attempted",
      "slug_name": "submissions-attempted",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Takedowns Defended",
      "slug_name": "takedowns-defended",
      "rounds": [
        {
          "red": 0,
          "blue": 0
        }
      ]
    },
    {
      "stats_name": "Cage Control",
      "slug_name": "cage-control",
      "rounds": [
        {
          "red": "0",
          "blue": "0"
        }
      ]
    },
    {
      "stats_name": "Ground Control",
      "slug_name": "ground-control",
      "rounds": [
        {
          "red": "0",
          "blue": "0"
        }
      ]
    }
  ]
```


Parameter | Type | Description
--------- | ------- | -----------
`stats_name` | string | ...
`stats_name` | rounds | ...
`red` | string | ...
`blue` | string | ...
