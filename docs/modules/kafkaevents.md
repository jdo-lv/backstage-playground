# LiveCasino Kafka events

The LiveCasino service is producer of Kafka events to two different external
services.

The service produces the static data to Lemur system in the [LiveCasinoStaticData](https://github.com/gutro/Platform-Gaming-Api/blob/master/src/main/avro/livecasino/event.livecasino-static-data.avsc) event.
The service produces the dynamic data to Frontend Integration system in the [LiveCasinoDynamicData](https://github.com/gutro/Platform-Gaming-Api/blob/master/src/main/avro/livecasino/event.livecasino-dynamic-data.avsc)

For more detail visit the Overview High Level block diagram.