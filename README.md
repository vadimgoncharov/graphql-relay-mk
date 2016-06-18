# React GraphQL and Relay MK
## Plan

* [x] First Part (11:00 - 12:15)
  * [x] GraphQL
    * [x] Queries
    * [x] Type System
      * [x] Schema
      * [x] Scalar
        * [x] Int
        * [x] Float
        * [x] String
        * [x] Boolean
        * [x] ID
      * [x] Object
      * [x] Interface ~
      * [x] Union ~
      * [x] Enum ~
      * [X] List
      * [x] NonNull
    * [x] Introspection
    * [x] Arguments
    * [x] Mutations
    * [x] Aliases
    * [x] Fragments
    * [x] Type Conditions
    * [x] Variables
      * [x] Default Values
    * [x] Interfaces
    * [x] Directives
    * [x] Deprecations
* [x] Second Part (12:30 - 13:45)
  * [x] Relay
    * [x] Containers
      * [x] Relay.QL
    * [x] Babel Relay Plugin
    * [x] RootContainer / Renderer
    * [x] Route
    * [x] Ready State
    * [x] Mutations
    * [x] Network Layer
    * [x] GraphQL Relay Specification
      * [x] Object Identification
      * [x] Connection
      * [x] Mutations
* [x] Third Part (15:00 - 16:15)
  * [x] List
  * [x] Pagination
  * [x] Load Old
  * [ ] Comments
    * [ ] Optimistic Updates
  * [ ] Likes
    * [ ] Error Handling
  * [ ] Pagination
  * [ ] State Synchronization
* [ ] Last Part (16:30 - 17:45)
 
## Example
http://graphql-swapi.parseapp.com/

```
{
  allFilms {
    edges {
      node {
        title
        ...FilmView
      }
    }
  }
}

fragment FilmView on Film {
  starshipConnection {
    edges {
      node {
        name
      }
    }
  }
}
```

Result: 
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "title": "A New Hope",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                },
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                },
                {
                  "node": {
                    "name": "Sentinel-class landing craft"
                  }
                },
                {
                  "node": {
                    "name": "Death Star"
                  }
                },
                {
                  "node": {
                    "name": "Millennium Falcon"
                  }
                },
                {
                  "node": {
                    "name": "Y-wing"
                  }
                },
                {
                  "node": {
                    "name": "X-wing"
                  }
                },
                {
                  "node": {
                    "name": "TIE Advanced x1"
                  }
                },
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                },
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                },
                {
                  "node": {
                    "name": "Sentinel-class landing craft"
                  }
                },
                {
                  "node": {
                    "name": "Death Star"
                  }
                },
                {
                  "node": {
                    "name": "Millennium Falcon"
                  }
                },
                {
                  "node": {
                    "name": "Y-wing"
                  }
                },
                {
                  "node": {
                    "name": "X-wing"
                  }
                },
                {
                  "node": {
                    "name": "TIE Advanced x1"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "title": "The Empire Strikes Back",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                },
                {
                  "node": {
                    "name": "Millennium Falcon"
                  }
                },
                {
                  "node": {
                    "name": "Y-wing"
                  }
                },
                {
                  "node": {
                    "name": "X-wing"
                  }
                },
                {
                  "node": {
                    "name": "Executor"
                  }
                },
                {
                  "node": {
                    "name": "Rebel transport"
                  }
                },
                {
                  "node": {
                    "name": "Slave 1"
                  }
                },
                {
                  "node": {
                    "name": "Imperial shuttle"
                  }
                },
                {
                  "node": {
                    "name": "EF76 Nebulon-B escort frigate"
                  }
                },
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                },
                {
                  "node": {
                    "name": "Millennium Falcon"
                  }
                },
                {
                  "node": {
                    "name": "Y-wing"
                  }
                },
                {
                  "node": {
                    "name": "X-wing"
                  }
                },
                {
                  "node": {
                    "name": "Executor"
                  }
                },
                {
                  "node": {
                    "name": "Rebel transport"
                  }
                },
                {
                  "node": {
                    "name": "Slave 1"
                  }
                },
                {
                  "node": {
                    "name": "Imperial shuttle"
                  }
                },
                {
                  "node": {
                    "name": "EF76 Nebulon-B escort frigate"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "title": "Return of the Jedi",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                },
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                },
                {
                  "node": {
                    "name": "Millennium Falcon"
                  }
                },
                {
                  "node": {
                    "name": "Y-wing"
                  }
                },
                {
                  "node": {
                    "name": "X-wing"
                  }
                },
                {
                  "node": {
                    "name": "Executor"
                  }
                },
                {
                  "node": {
                    "name": "Rebel transport"
                  }
                },
                {
                  "node": {
                    "name": "Imperial shuttle"
                  }
                },
                {
                  "node": {
                    "name": "EF76 Nebulon-B escort frigate"
                  }
                },
                {
                  "node": {
                    "name": "Calamari Cruiser"
                  }
                },
                {
                  "node": {
                    "name": "A-wing"
                  }
                },
                {
                  "node": {
                    "name": "B-wing"
                  }
                },
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                },
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                },
                {
                  "node": {
                    "name": "Millennium Falcon"
                  }
                },
                {
                  "node": {
                    "name": "Y-wing"
                  }
                },
                {
                  "node": {
                    "name": "X-wing"
                  }
                },
                {
                  "node": {
                    "name": "Executor"
                  }
                },
                {
                  "node": {
                    "name": "Rebel transport"
                  }
                },
                {
                  "node": {
                    "name": "Imperial shuttle"
                  }
                },
                {
                  "node": {
                    "name": "EF76 Nebulon-B escort frigate"
                  }
                },
                {
                  "node": {
                    "name": "Calamari Cruiser"
                  }
                },
                {
                  "node": {
                    "name": "A-wing"
                  }
                },
                {
                  "node": {
                    "name": "B-wing"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "title": "The Phantom Menace",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "name": "Republic Cruiser"
                  }
                },
                {
                  "node": {
                    "name": "Droid control ship"
                  }
                },
                {
                  "node": {
                    "name": "Naboo fighter"
                  }
                },
                {
                  "node": {
                    "name": "Naboo Royal Starship"
                  }
                },
                {
                  "node": {
                    "name": "Scimitar"
                  }
                },
                {
                  "node": {
                    "name": "Republic Cruiser"
                  }
                },
                {
                  "node": {
                    "name": "Droid control ship"
                  }
                },
                {
                  "node": {
                    "name": "Naboo fighter"
                  }
                },
                {
                  "node": {
                    "name": "Naboo Royal Starship"
                  }
                },
                {
                  "node": {
                    "name": "Scimitar"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "title": "Attack of the Clones",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "name": "Slave 1"
                  }
                },
                {
                  "node": {
                    "name": "Droid control ship"
                  }
                },
                {
                  "node": {
                    "name": "Naboo fighter"
                  }
                },
                {
                  "node": {
                    "name": "J-type diplomatic barge"
                  }
                },
                {
                  "node": {
                    "name": "AA-9 Coruscant freighter"
                  }
                },
                {
                  "node": {
                    "name": "Jedi starfighter"
                  }
                },
                {
                  "node": {
                    "name": "H-type Nubian yacht"
                  }
                },
                {
                  "node": {
                    "name": "Republic Assault ship"
                  }
                },
                {
                  "node": {
                    "name": "Solar Sailer"
                  }
                },
                {
                  "node": {
                    "name": "Slave 1"
                  }
                },
                {
                  "node": {
                    "name": "Droid control ship"
                  }
                },
                {
                  "node": {
                    "name": "Naboo fighter"
                  }
                },
                {
                  "node": {
                    "name": "J-type diplomatic barge"
                  }
                },
                {
                  "node": {
                    "name": "AA-9 Coruscant freighter"
                  }
                },
                {
                  "node": {
                    "name": "Jedi starfighter"
                  }
                },
                {
                  "node": {
                    "name": "H-type Nubian yacht"
                  }
                },
                {
                  "node": {
                    "name": "Republic Assault ship"
                  }
                },
                {
                  "node": {
                    "name": "Solar Sailer"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "title": "Revenge of the Sith",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                },
                {
                  "node": {
                    "name": "Droid control ship"
                  }
                },
                {
                  "node": {
                    "name": "Jedi starfighter"
                  }
                },
                {
                  "node": {
                    "name": "Trade Federation cruiser"
                  }
                },
                {
                  "node": {
                    "name": "Theta-class T-2c shuttle"
                  }
                },
                {
                  "node": {
                    "name": "Republic attack cruiser"
                  }
                },
                {
                  "node": {
                    "name": "Naboo star skiff"
                  }
                },
                {
                  "node": {
                    "name": "Jedi Interceptor"
                  }
                },
                {
                  "node": {
                    "name": "arc-170"
                  }
                },
                {
                  "node": {
                    "name": "Banking clan frigte"
                  }
                },
                {
                  "node": {
                    "name": "Belbullab-22 starfighter"
                  }
                },
                {
                  "node": {
                    "name": "V-wing"
                  }
                },
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                },
                {
                  "node": {
                    "name": "Droid control ship"
                  }
                },
                {
                  "node": {
                    "name": "Jedi starfighter"
                  }
                },
                {
                  "node": {
                    "name": "Trade Federation cruiser"
                  }
                },
                {
                  "node": {
                    "name": "Theta-class T-2c shuttle"
                  }
                },
                {
                  "node": {
                    "name": "Republic attack cruiser"
                  }
                },
                {
                  "node": {
                    "name": "Naboo star skiff"
                  }
                },
                {
                  "node": {
                    "name": "Jedi Interceptor"
                  }
                },
                {
                  "node": {
                    "name": "arc-170"
                  }
                },
                {
                  "node": {
                    "name": "Banking clan frigte"
                  }
                },
                {
                  "node": {
                    "name": "Belbullab-22 starfighter"
                  }
                },
                {
                  "node": {
                    "name": "V-wing"
                  }
                }
              ]
            }
          }
        }
      ]
    }
  }
}
```

Arguments:
```
{
	allFilms(first: 1) {
    edges {
      node {
        title 
      }
    }
  }
}
```

Result:
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "title": "A New Hope"
          }
        }
      ]
    }
  }
}
```

```
{
  __schema {
    types{
      name
      fields {
        name
        type {
          name
          fields {
            name
          }
        }
      }
    }
  }
}
```

Result
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "title": "A New Hope"
          }
        },
        {
          "node": {
            "title": "The Empire Strikes Back"
          }
        },
        {
          "node": {
            "title": "Return of the Jedi"
          }
        },
        {
          "node": {
            "title": "The Phantom Menace"
          }
        },
        {
          "node": {
            "title": "Attack of the Clones"
          }
        },
        {
          "node": {
            "title": "Revenge of the Sith"
          }
        }
      ]
    }
  }
}
```

Mutations:
```
mutation QQQ {
  updateStarship(newName: "yyy") {
    starship {
      name
    }
  }
}
```

Alias:
```
{
  allFilms {
    edges {
      node {
        firstStarship: starshipConnection(first:1) {
          edges {
            node {
              name
            }
          }
        }
        lastStarship: starshipConnection(last:1) {
          edges {
            node {
              name
            }
          }
        }
      }
    }
  }
}
```

Result:
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "firstStarship": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                }
              ]
            },
            "lastStarship": {
              "edges": [
                {
                  "node": {
                    "name": "TIE Advanced x1"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "firstStarship": {
              "edges": [
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                }
              ]
            },
            "lastStarship": {
              "edges": [
                {
                  "node": {
                    "name": "EF76 Nebulon-B escort frigate"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "firstStarship": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                }
              ]
            },
            "lastStarship": {
              "edges": [
                {
                  "node": {
                    "name": "B-wing"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "firstStarship": {
              "edges": [
                {
                  "node": {
                    "name": "Republic Cruiser"
                  }
                }
              ]
            },
            "lastStarship": {
              "edges": [
                {
                  "node": {
                    "name": "Scimitar"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "firstStarship": {
              "edges": [
                {
                  "node": {
                    "name": "Slave 1"
                  }
                }
              ]
            },
            "lastStarship": {
              "edges": [
                {
                  "node": {
                    "name": "Solar Sailer"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "firstStarship": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                }
              ]
            },
            "lastStarship": {
              "edges": [
                {
                  "node": {
                    "name": "V-wing"
                  }
                }
              ]
            }
          }
        }
      ]
    }
  }
}
```

Fragment:
```
{
  allFilms {
    edges {
      node {
        ...MainList
        ...LastList
      }
    }
  }
}

fragment MainList on Film {
  first: starshipConnection(first:1) {
    edges {
      node {
        name
      }
    }
  }
}


fragment LastList on Film {
  last: starshipConnection(last:1) {
    edges {
      node {
        name
      }
    }
  }
}
```

Result:
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "first": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                }
              ]
            },
            "last": {
              "edges": [
                {
                  "node": {
                    "name": "TIE Advanced x1"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "first": {
              "edges": [
                {
                  "node": {
                    "name": "Star Destroyer"
                  }
                }
              ]
            },
            "last": {
              "edges": [
                {
                  "node": {
                    "name": "EF76 Nebulon-B escort frigate"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "first": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                }
              ]
            },
            "last": {
              "edges": [
                {
                  "node": {
                    "name": "B-wing"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "first": {
              "edges": [
                {
                  "node": {
                    "name": "Republic Cruiser"
                  }
                }
              ]
            },
            "last": {
              "edges": [
                {
                  "node": {
                    "name": "Scimitar"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "first": {
              "edges": [
                {
                  "node": {
                    "name": "Slave 1"
                  }
                }
              ]
            },
            "last": {
              "edges": [
                {
                  "node": {
                    "name": "Solar Sailer"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "first": {
              "edges": [
                {
                  "node": {
                    "name": "CR90 corvette"
                  }
                }
              ]
            },
            "last": {
              "edges": [
                {
                  "node": {
                    "name": "V-wing"
                  }
                }
              ]
            }
          }
        }
      ]
    }
  }
}
```

Type Conditions:
```
{
  node(id:"c3RhcnNoaXBzOjI==") {
    id
    ... on Film {
      title
    }
    ... on Starship  {
      name
    }
  }
  allFilms {
    edges {
      node {
       id
        starshipConnection {
          edges {
            node {
              id
            }
          }
        }
      }
    }
  }
}

```

Result:
```
{
  "data": {
    "node": {
      "id": "c3RhcnNoaXBzOjI=",
      "name": "CR90 corvette"
    },
    "allFilms": {
      "edges": [
        {
          "node": {
            "id": "ZmlsbXM6MQ==",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjU="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjk="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjU="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjk="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEz"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "id": "ZmlsbXM6Mg==",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIz"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "id": "ZmlsbXM6Mw==",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjEy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjE3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI5"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "id": "ZmlsbXM6NA==",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQw"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQx"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "id": "ZmlsbXM6NQ==",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjUy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjU4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjIx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjM5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ3"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjUy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjU4"
                  }
                }
              ]
            }
          }
        },
        {
          "node": {
            "id": "ZmlsbXM6Ng==",
            "starshipConnection": {
              "edges": [
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjU5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjYx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjYz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY0"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY2"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjc0"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjc1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjI="
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjMy"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjQ4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjU5"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjYx"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjYz"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY0"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY1"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY2"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjY4"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjc0"
                  }
                },
                {
                  "node": {
                    "id": "c3RhcnNoaXBzOjc1"
                  }
                }
              ]
            }
          }
        }
      ]
    }
  }
}
```

Variables:
```
query SomeQueryName($first: Int = 1) {
  allFilms(first: $first){
    edges {
      node {
        title
      }
    }
  }
}
```

Query:
```
{
  "first": 3
}
```


Result: 
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "title": "A New Hope"
          }
        },
        {
          "node": {
            "title": "The Empire Strikes Back"
          }
        },
        {
          "node": {
            "title": "Return of the Jedi"
          }
        }
      ]
    }
  }
}
```

Directives:
```
query SkipableStarship($skipStarship:Boolean!)
{
  allFilms {
    edges {
      node{
        title
        starshipConnection(first: 1) @skip(if:$skipStarship) {
          edges {
            node {
              name
            }
          }
        }
      }
    }
  }
}
```

Query:
```
{
  "skipStarship": true
}
```

Result:
```
{
  "data": {
    "allFilms": {
      "edges": [
        {
          "node": {
            "title": "A New Hope"
          }
        },
        {
          "node": {
            "title": "The Empire Strikes Back"
          }
        },
        {
          "node": {
            "title": "Return of the Jedi"
          }
        },
        {
          "node": {
            "title": "The Phantom Menace"
          }
        },
        {
          "node": {
            "title": "Attack of the Clones"
          }
        },
        {
          "node": {
            "title": "Revenge of the Sith"
          }
        }
      ]
    }
  }
}
```



## GraphQL Spec
https://facebook.github.io/graphql/

### Integer
Numeric integer values larger than 32‐bit should either use String or a custom‐defined Scalar type, as not all platforms and transports support encoding integer numbers larger than 32‐bit.
