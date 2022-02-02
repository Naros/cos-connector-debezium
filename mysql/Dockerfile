ARG DEBEZIUM_VERSION=1.9.0.Alpha1
ARG STRIMZI_VERSION=latest
ARG KAFKA_VERSION=3.0.0

FROM quay.io/debezium/connect:${DEBEZIUM_VERSION} as upstream
FROM quay.io/strimzi/kafka:${STRIMZI_VERSION}-kafka-${KAFKA_VERSION}

COPY --from=upstream /kafka/connect/debezium-connector-mysql/ /opt/kafka/plugins/debezium-connector-mysql/

USER 1001