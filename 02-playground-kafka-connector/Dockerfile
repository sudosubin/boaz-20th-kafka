FROM confluentinc/cp-kafka-connect-base:7.0.9

WORKDIR /home/appuser

RUN confluent-hub install --no-prompt confluentinc/kafka-connect-s3:10.4.3

COPY src/connect-plaintext-input-to-s3.json ./connect-plaintext-input-to-s3.json
COPY src/entrypoint.sh ./entrypoint.sh

CMD ["./entrypoint.sh"]
