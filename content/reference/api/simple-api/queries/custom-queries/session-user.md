---
alias: gieh7iw2ru
path: /docs/reference/simple-api/session-user
layout: REFERENCE
shorttitle: The authenticated user
description: Query the signed in user in the Simple API. The user needs to be registered with an authentication provider like Auth0 in your GraphQL backend.
simple_relay_twin: peyaaph9vi
tags:
  - simple-api
  - queries
  - authentication
  - session-user
related:
  further:
    - wejileech9
    - iegoo0heez
    - eetai5meic
    - eixu9osueb
  more:
    - goij0cooqu
    - cahzai2eur
---

# The Authenticated User in the Simple API

If the request of a query or mutation contains authentication information on the [session user](!alias-geekae9gah#user-login), you can use the `user` query to query information on that user. All fields of the `User` type are available. Depending on the [auth providers](!alias-seimeish6e#authentication-providers) you enabled, you can additionally include different fields in the query.

```graphql
---
endpoint: https://api.graph.cool/simple/v1/cixne4sn40c7m0122h8fabni1
disabled: true
---
query {
  user {
    id
  }
}
---
{
  "data": {
    "user": {
      "id": "my-user-id"
    }
  }
}
```

If no user is signed in, the query response will look like this:

```graphql
---
endpoint: https://api.graph.cool/simple/v1/cixne4sn40c7m0122h8fabni1
disabled: true
---
query {
  user {
    id
  }
}
---
{
  "data": {
    "user": null
  }
}
```

Note that you have to set appropriate [permissions](!alias-iegoo0heez) on the `User` type to use the `user` query.
