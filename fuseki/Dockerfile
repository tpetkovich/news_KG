FROM secoresearch/fuseki:5.0.0

COPY --chown=9008 /news_kg.ttl /tmp/
COPY --chown=9008 /assembler.ttl /fuseki-base/configuration/

RUN $JAVA_CMD tdb2.tdbloader --loc /fuseki-base/databases/news_kg /tmp/news_kg.ttl \
	&& $TEXTINDEXER