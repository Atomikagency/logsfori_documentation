# WeWeb Integration

## Introduction

LogsForI provides a flexible integration with WeWeb, allowing you complete control over the logs and timers sent from your WeWeb workflows directly to your LogsForI dashboard. As WeWeb doesn't offer automatic log retrieval, this integration relies on manual setup, giving you precise control over the data you track and send.

This integration is ideal if you're looking for detailed, custom logging within your WeWeb application.

---

## Setup

### Create a connection

In your LogsForI project, click on the **"Connections"** tab in the sidebar, then select **"New connection"** in the top-right corner. Find the WeWeb integration and click **"Connect"**.

The WeWeb connection page will open, asking you to provide a name for your connection. Before you finalize the creation, copy the **token** displayed on this page—you'll need it for sending logs and timers through your WeWeb workflows. If you lose this token, you can always retrieve it by editing the connection from your connections list.

---

## Send logs and timers via WeWeb workflows

With your connection created and your token copied, you can now configure your WeWeb workflows to send data to LogsForI:

- Within your WeWeb workflows, use the built-in **"REST API Request"** action.
- Configure this action according to the LogsForI API endpoints:
  - [Push Logs documentation](/api-reference/push-log.md)
  - [Push Timers documentation](/api-reference/push-timer.md)

Make sure to include your unique token in the API request to ensure proper authentication and correct data association with your connection.

---

## It's ready!
Your WeWeb integration is now fully configured. Start sending custom logs and timers, gain deep insights, and effectively monitor your application's performance and behavior directly from your LogsForI dashboard.

