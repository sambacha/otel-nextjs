### Tracing

#### Steps to use tracing

1. Run the zipkin client using docker

    ```
    docker run -d -p 9411:9411 openzipkin/zipkin
    ```

2. Enable tracing 

    ```typescript
    const client = new web3Client({
      ...,
      tracingEnabled: true
    })
    ```

    Or you can turn on tracing while running the `Web3Client` by calling the `tracingEnabled` method of `web3Client`.

    ```typescript
    // Turn tracing off
    client.tracingEnabled(false);
    ```

3. Once you run the app and started producing logs, go to zipkin client which is running on `http://localhost:9411`. There you can click `RUN QUERY` button without any filters to show all the logs.
