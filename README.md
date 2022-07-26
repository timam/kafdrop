docker run  -p 9000:9000 \
    -e KAFKA_BROKERCONNECT=b-1.________.amazonaws.com:9094,b-2.________.amazonaws.com:9094,b-3.________.amazonaws.com:9094 \
    -e JVM_OPTS="-Xms32M -Xmx64M" \
    -e SERVER_SERVLET_CONTEXTPATH="/" \
   -e KAFKA_PROPERTIES="$(cat kafka.properties | base64)" \
    obsidiandynamics/kafdrop
