# GET - Fetch user blood glucose levels

Before we start, to use this calls you'll need to be logged in and generated a token. See [[GET - Login]] for more info.

You can fetch the user data, including the blood glucose values that you have submitted with [[API/METHODS/GET - Submit blood glucose value]]

Remember that `"logtype_id": 1` means that it's a record of type blood glucose level.

```shell
START_DATE='2021-08-09%2000:00:00'
END_DATE='2021-08-12%2000:10:00'
curl "https://api.jadediabetes.com/api/1.0/extract.json?token=${API_TOKEN}&start_date=${START_DATE}&end_date=${END_DATE}&page="
```
Response:
```json
{
  "logs": [
    {
      "log_id": 5549737810,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-09 00:00:00",
      "created": "2021-08-10 09:30:14",
      "updated": null,
      "value": 5,
      "notes": "none"
    },
    {
      "log_id": 5549659973,
      "user_id": 35963,
      "logtype_id": 23,
      "other": 0,
      "time": "2021-08-10 07:38:52",
      "created": "2021-08-10 07:38:52",
      "updated": null,
      "value": 0,
      "notes": "Target BGL changed to  (by )"
    },
    {
      "log_id": 5549659978,
      "user_id": 35963,
      "logtype_id": 23,
      "other": 0,
      "time": "2021-08-10 07:38:52",
      "created": "2021-08-10 07:38:52",
      "updated": null,
      "value": 5,
      "notes": "Dawn phenomenon changed to "
    },
    {
      "log_id": 5549659977,
      "user_id": 35963,
      "logtype_id": 23,
      "other": 0,
      "time": "2021-08-10 07:38:52",
      "created": "2021-08-10 07:38:52",
      "updated": null,
      "value": 4,
      "notes": "Basal rate changed to "
    },
    {
      "log_id": 5549659976,
      "user_id": 35963,
      "logtype_id": 23,
      "other": 0,
      "time": "2021-08-10 07:38:52",
      "created": "2021-08-10 07:38:52",
      "updated": null,
      "value": 3,
      "notes": "Target BGL changed to "
    },
    {
      "log_id": 5549659975,
      "user_id": 35963,
      "logtype_id": 23,
      "other": 0,
      "time": "2021-08-10 07:38:52",
      "created": "2021-08-10 07:38:52",
      "updated": null,
      "value": 0,
      "notes": "Dawn phenomenon changed to  (by )"
    },
    {
      "log_id": 5549659974,
      "user_id": 35963,
      "logtype_id": 23,
      "other": 0,
      "time": "2021-08-10 07:38:52",
      "created": "2021-08-10 07:38:52",
      "updated": null,
      "value": 0,
      "notes": "Basal rate changed to  (by )"
    },
    {
      "log_id": 5549689411,
      "user_id": 35963,
      "logtype_id": 1,
      "other": -126,
      "time": "2021-08-10 08:19:42",
      "created": "2021-08-10 08:19:42",
      "updated": null,
      "value": 40,
      "notes": "no notes"
    },
    {
      "log_id": 5549714307,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 08:55:39",
      "created": "2021-08-10 08:55:39",
      "updated": null,
      "value": 40,
      "notes": "none"
    },
    {
      "log_id": 5549721097,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:05:35",
      "created": "2021-08-10 09:05:35",
      "updated": null,
      "value": 40,
      "notes": "none"
    },
    {
      "log_id": 5549721693,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 126,
      "time": "2021-08-10 09:06:32",
      "created": "2021-08-10 09:06:32",
      "updated": null,
      "value": 5,
      "notes": "none"
    },
    {
      "log_id": 5549724712,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:10:42",
      "created": "2021-08-10 09:10:42",
      "updated": null,
      "value": 5,
      "notes": "none"
    },
    {
      "log_id": 5549731302,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:20:11",
      "created": "2021-08-10 09:20:11",
      "updated": null,
      "value": 5,
      "notes": "none"
    },
    {
      "log_id": 5549731378,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:20:26",
      "created": "2021-08-10 09:20:26",
      "updated": null,
      "value": 5,
      "notes": ""
    },
    {
      "log_id": 5549731384,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:20:32",
      "created": "2021-08-10 09:20:32",
      "updated": null,
      "value": 5.1,
      "notes": ""
    },
    {
      "log_id": 5549731388,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:20:40",
      "created": "2021-08-10 09:20:40",
      "updated": null,
      "value": 5.1,
      "notes": ""
    },
    {
      "log_id": 5549732409,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:22:49",
      "created": "2021-08-10 09:22:49",
      "updated": null,
      "value": 5.1,
      "notes": ""
    },
    {
      "log_id": 5549732702,
      "user_id": 35963,
      "logtype_id": 1,
      "other": 1,
      "time": "2021-08-10 09:23:02",
      "created": "2021-08-10 09:23:02",
      "updated": null,
      "value": 5.1,
      "notes": ""
    }
  ],
  "rows": 18,
  "max_logs": 100,
  "logs_deleted": [

  ],
  "rows_deleted": 0,
  "result": true,
  "message": "Ok"
}%
```


You can paginate the results, but only if you have more than 100 records, since each page shows 100 records it seems.

```shell
START_DATE='2021-08-09%2000:00:00'
END_DATE='2021-08-12%2000:10:00'
PAGE='1'
curl "https://api.jadediabetes.com/api/1.0/extract.json?token=${API_TOKEN}&start_date=${START_DATE}&end_date=${END_DATE}&page=${PAGE}"
```