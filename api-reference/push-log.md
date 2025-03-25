# Push Log

## Introduction

The LogsForI API allows you to manually send custom log entries directly to your LogsForI dashboard, giving you full and flexible control over your tracking data. This API is particularly useful when automatic log retrieval isn't available or when integrating with custom-coded applications.

---

## API Endpoint

```
POST https://api.logsfori.com/push-log
```

---

## Request Body

| Parameter        | Type     | Description                                                       | Required | Default |
| ---------------- | -------- | ----------------------------------------------------------------- | -------- | ------- |
| `token`          | `string` | Your LogsForI token, provided during connection creation          | Yes      | -       |
| `event_name`     | `string` | A descriptive name representing the logged event                  | No       | -       |
| `message`        | `string` | Your custom log message                                           | No       | -       |
| `severity`       | `string` | Log severity (`info`, `warning`, `error`, `critical`, or `debug`) | No       | `info`  |
| `transaction_id` | `string` | Transaction ID related to the log event                           | No       | -       |
| `resource_id`    | `string` | Resource ID associated with the log event                         | No       | -       |
| `execution_time` | `number` | Execution time in milliseconds                                    | No       | -       |
| `extra`          | `object` | Any additional data you want to include                           | No       | -       |
| `created_at`     | `number` | Custom timestamp (milliseconds since epoch UTC)                   | No       | `now`   |

### Example Request

```curl
curl --location 'https://api.logsfori.com/push-log' \
--header 'Content-Type: application/json' \
--data-raw '{
    "token": "your-logsfori-token",
    "event_name": "user_registration",
    "message": "New user registered successfully",
    "severity": "info",
    "transaction_id": "tx123456",
    "resource_id": "user789",
    "execution_time": 350,
    "extra": {
        "user_id": "user789",
        "email": "john.doe@example.com",
        "first_name": "John",
        "last_name": "Doe"
    },
    "created_at": 1742379826000
}'
```

---

## Response

| Status | Body (json)                                              | Description                                                |
| ------ | -------------------------------------------------------- | ---------------------------------------------------------- |
| `202`  | `{"status": "accepted"}`                                 | Your log has been accepted                                 |
| `403`  | `{"status": "Invalid token"}`                            | Your LogsForI token is invalid or missing                  |
| `429`  | `{"status": "Quota exceeded. Update your subscription"}` | You have exceeded your log quota. Update your subscription |
