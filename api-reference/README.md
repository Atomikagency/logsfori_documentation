# API Reference

## Introduction
LogsForI provides a simple API that lets you easily push custom logs and timers directly into your project.[Visiter LogsForI](https://logsfori.com)

While our system automatically retrieves `logs` and `timers` for many integrations, there are times when manually sending custom data can be really useful. That’s why, whenever you create a new connection -regardless of the integration- you’ll receive a token to manually send your data. You can also find this token anytime on the connection editing page.


## Why an API Token for each connection?
Let's say you're using the [Bubble integration](/integration/bubble.md), which has automatic log retrieval. You don't need to create a separate [API](/integration/api.md) connection to send logs manually, because a specific token linked to your [Bubble](/integration/bubble.md) connection is generated automatically. By using this token —say, in a specific workflow— your logs will be clearly identified as coming from your [Bubble integration](/integration/bubble.md), keeping them neatly categorized and easy to understand.

## Why doesn't my integration retrieve logs automatically?
For some integrations —like [WeWeb integration](/integration/weweb.md), for example— there's no built-in logging system or API allowing our platform to retrieve logs automatically. In these cases, we still provide you with a dedicated connection to categorize and easily identify where your logs come from. However, the usage remains similar to an [API](/integration/api.md) connection: you'll need to manually send logs wherever it makes sense in your project, just as you would with a custom-coded application.