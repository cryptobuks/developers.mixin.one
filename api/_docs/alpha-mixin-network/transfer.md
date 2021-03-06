---
title: Transfer
category: Mixin Network
order: 23
---

Transfer of assets between Mixin Network users.

###### POST /transfers

| asset_id | String: UUID |
| opponent_id | String: UUID |
| amount | String: e.g.: "0.01" |
| pin | String: Encrypted Pin |
| trace_id | String: UUID |
| memo | String: Max 140 characters, e.g.: "transfer to you" |

```
// cURL Example
curl -i -H "Content-Type: application/json" -H "Authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1MzMxMTgwODIsImlhdCI6MTUyNTM0MjA4MiwianRpIjoiMmQ5YjI2YTUtMDc4Ny00OGIyLWExN2MtNWM5ZGQ5Mjc5MDI2Iiwic2lkIjoiYTM0YzA3YTktNzU1ZC00YjU0LTk0YzUtZTQ1ZTlhMmRkNDNlIiwic2lnIjoiMTUzMjIwNDlkNWFlMzNhNjYyMjAwOWQ1YTk4N2ZjYmRlNDQ4OTkxMmUxZmE2ZTAwODk0YjlhYzM2MTRiZTE4MiIsInVpZCI6IjA2YWVkMWUzLWJkNzctNGE1OS05OTFhLTViYjVhZTZmYmIwOSJ9.RVR6ejUZkAGeRG9M9C5Jk4llmJvFHTXAx3f3yxwTiiglFbfiNrt2fI9ZHNYCp7XbJJh4w9ECyX1K8Obgq7ep2RcGzjMkKWlXWuECLwgUA4FRFrewvPcH2Edplo61B9I6M89Ohi1_V6owkee08bDR2k0se2MdWTxnHca8BzOFckc" "https://api.mixin.one/transfers" -XPOST --data '{"amount":"10","asset_id":"43d61dcd-e413-450d-80b8-101d5e903357","opponent_id":"a465ffdb-4441-4cb9-8b45-00cf79dfbc46","memo":"hello","pin":"F39IsJmUaZW03VMV/01lHyY2RCoZ7/X764akX+EmthIc4uVsWAWQTM/IxX5Z9C1y","trace_id":"7c67e8e8-b142-488b-80a3-61d4d29c90bf"}'
```

```
// Sample Response
{  
  "data":{  
    "type":"transfer",
      "snapshot_id":"ab56be4c-5b20-41c6-a9c3-244f9a433f35",
      "opponent_id":"a465ffdb-4441-4cb9-8b45-00cf79dfbc46",
      "asset_id":"43d61dcd-e413-450d-80b8-101d5e903357",
      "amount":"-10",
      "trace_id":"7c67e8e8-b142-488b-80a3-61d4d29c90bf",
      "memo":"hello",
      "created_at":"2018-05-03T10:08:34.859542588Z"
  }
}
```
