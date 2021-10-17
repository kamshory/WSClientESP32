# WSClientESP32

When ESP32 is connected to a WebSocket server, the process generally runs asynchronously. But what if the message publisher requires a response for every request sent?

The publisher of the message must submit a topic with a unique name for each request. The publisher then acts as a subscriber with the submitted topic. Similarly, ESP32 which initially acts as a subscriber will publish messages according to the topics requested by the publisher. Thus, M2M communication here seems to run synchronously.

Publishers do not need to submit topic names for response if publishers do not expect a response from ESP32. Thus, M2M communication here will be asynchronous.
