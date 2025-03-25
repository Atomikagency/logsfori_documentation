# API Integration

## Introduction

LogsForI provides a simple and powerful API integration that allows you to have complete control over the logs and timers sent to your LogsForI dashboard. Unlike automatic integrations, the API integration requires manual configuration, giving you full flexibility on what events to track and how to categorize them.

This integration is especially useful for custom applications or platforms that don't support automatic log retrieval, enabling detailed and precise monitoring tailored exactly to your project's needs.

---

## Setup

### Create a connection

On your LogsForI project, click on the **"Connections"** tab in the sidebar, then click on the **"New connection"** button at the top right corner. Here you'll see all available integrations. Click on **"Connect"** on the API integration card.

The API connection page will open, asking you to provide a name for your connection. Before creating the connection, copy the **token** displayed on this page—this **token** is essential for sending logs and timers through our API.

If you lose the **token**, you can always retrieve it later by editing the connection from your connections list.

---

## Send logs and timers via API

Now that your connection is created and your token copied, you can start sending data directly to LogsForI using our API endpoints.

- To send logs, please refer to the [Push Logs documentation](/api-reference/push-log.md).
- To send timers, please refer to the [Push Timers documentation](/api-reference/push-timer.md).

Make sure to use your unique token for authentication in each API call to ensure your data is correctly associated with your connection.

---

## It's ready!
Your API integration is now fully set up. You can begin sending custom logs and timers, configuring your monitoring exactly the way you want, and start gaining valuable insights from your application's data.

