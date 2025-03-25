# Push Timer

## Introduction

The LogsForI API allows you to manually record the duration of specific events directly to your LogsForI dashboard. This API is particularly useful for performance monitoring, debugging, and analyzing critical processes within your custom-coded applications or when automatic timer tracking isn't available.

---

## API Endpoint

```
POST https://api.logsfori.com/timer
```

---

## Request Body

| Parameter        | Type     | Description                                                 | Required | Default |
| ---------------- | -------- | ----------------------------------------------------------- | -------- | ------- |
| `token`          | `string` | Your LogsForI token, provided during connection creation    | Yes      | -       |
| `func_name`      | `string` | A descriptive name representing the timed function or event | Yes      | -       |
| `execution_time` | `number` | Execution time in milliseconds                              | Yes      | -       |
| `created_at`     | `number` | Custom timestamp (milliseconds since epoch UTC)             | No       | `now`   |

### Example Request

```curl
curl --location 'https://api.logsfori.com/timer' \
--header 'Content-Type: application/json' \
--data-raw '{
    "token": "your-logsfori-token",
    "func_name": "data_import",
    "execution_time": 1200,
    "created_at": 1742379826000
}'
```

---

## Response

| Status | Body (json)                                              | Description                                                  |
| ------ | -------------------------------------------------------- | ------------------------------------------------------------ |
| `202`  | `{"status": "accepted"}`                                 | Your timer has been accepted                                 |
| `403`  | `{"status": "Invalid token"}`                            | Your LogsForI token is invalid or missing                    |
| `429`  | `{"status": "Quota exceeded. Update your subscription"}` | You have exceeded your timer quota. Update your subscription |
