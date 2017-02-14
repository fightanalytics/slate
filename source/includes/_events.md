
# Events

## Get All Events

```ruby
```


```javascript
```

> The above command returns JSON structured like this:

```json
{
  "title" : "UFC's events",
  "events" : [
    {
      "event_id" : "588fbc3191c1bd0a78859456",
      "data" : [
        {
          "name" : "UFC Fight Night 104",
          "date" : "02.04.2017",
          "location" : "Houston, Texas",
          "poster_image" : "url",
          "promotion" : "UFC"
        }
      ]
    },
    ...
  ]
}
```

This endpoint retrieves all events.

### HTTP Request

`GET http://api.fightanalytics.cc/v1/api/events`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
`event_id` | string | ...
`data` | array | ...
`date` | string | ...
`location` | string | ...
`poster_image` | string | ...
`promotion` | string | ...


## Get a Specific Event

```ruby
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
  "event_id" : "588fbc3191c1bd0a78859456",
  "data" : [
    {
      "name" : "UFC Fight Night 104",
      "date" : "02.04.2017",
      "location" : "Houston, Texas",
      "poster_image" : "url",
      "promotion" : "UFC"
    }
  ],
  "card" : [
    {
      "fight_id" : "588fbd7291c1bd0a7885945a",
      "fighter_red" : [
        {
          "fighter_id" : "56c2509e5ce43c5a0c69a18a",
          "first_name" : "Dennis",
          "last_name" : "Bermudez",
          "nick_name" : "The Menace",
          "profile_image" : "/uploads/thumb/Dennis-Bermudez_231392_FighterProfile_30.png",
          "body_image" : "/uploads/regular/Dennis-Bermudez_231392_LeftFullBodyImage.png",
          "record" : "16 / 5 / 0",
          "country" : "United-States"
        }
      ],
      "fighter_blue" : [
        {
          "fighter_id" : "588fbd1391c1bd0a78859459",
          "first_name" : "Chan",
          "last_name" : "Sung Jung",
          "nick_name" : "The Korean Zombie",
          "profile_image" : "/uploads/thumb/Chan-Sung-Jung_1160_FighterProfile_30.png",
          "body_image" : "/uploads/regular/Chan-Sung-Jung_1160_RightFullBodyImage.png",
          "record" : "13 / 4 / 0",
          "country" : "South-Korea"
        }
      ],
      "result" : [
        {
          "winner" : "blue",
          "winner_by" : "KO",
          "at_round" : "1",
          "at_time" : "2:29"
        }
      ]
    },
    ...
  ]
}
```

This endpoint retrieves a specific event.

### HTTP Request

`GET http://api.fightanalytics.cc/v1/api/events/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
`ID` | The ID of the event to retrieve


### Available Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
`event_id` | string | ...
`data` | array | ...
`name` | string | ...
`date` | string | ...
`location` | string | ...
`poster_image` | string | ...
`promotion` | string | ...
`card` | string | ...
`fight_id` | string | ...
`fighter_red` | string | ...
`fighter_id` | string | ...
`first_name` | string | ...
`last_name` | string | ...
`nick_name` | string | ...
`profile_image` | string | ...
`body_image` | string | ...
`record` | string | ...
`country` | string | ...
`fighter_blue` | string | ...
`fighter_id` | string | ...
`first_name` | string | ...
`last_name` | string | ...
`nick_name` | string | ...
`profile_image` | string | ...
`body_image` | string | ...
`record` | string | ...
`country` | string | ...
`result` | string | ...
`winner` | string | ...
`winner_by` | string | ...
`at_round` | string | ...
`at_time` | string | ...