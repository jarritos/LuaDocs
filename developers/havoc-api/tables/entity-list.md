---
description: Functions for getting entity objects.
---

# Entity list

Entity variables can get accessed in the [entity](../usertypes/entity/ "mention") sections

***

### get\_entity

{% code overflow="wrap" lineNumbers="true" %}
```lua
entity_list.get_entity([int] player_index): [player]
```
{% endcode %}

| Arguments     | Type    | Desc                       |
| ------------- | ------- | -------------------------- |
| player\_index | integer | index of a specific player |

Returns a player object for the given index.

***

### get\_local\_index

{% code overflow="wrap" lineNumbers="true" %}
```lua
entity_list.get_local_index(): [int]
```
{% endcode %}

Returns local players index.

***

### get\_max\_clients

{% code overflow="wrap" lineNumbers="true" %}
```lua
entity_list.get_max_clients(): [int] 
```
{% endcode %}

Returns the index of the highest PLAYER index.

***

### get\_highest\_entity\_index

{% code overflow="wrap" lineNumbers="true" %}
```lua
entity_list.get_highest_entity_index(): [int] 
```
{% endcode %}

Returns the index of the highest ENTITY index.

***
