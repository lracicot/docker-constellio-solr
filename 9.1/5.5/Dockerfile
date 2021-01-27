# ---------- Source ---------- #
FROM alpine AS source
RUN apk add git
RUN git clone --depth 1 --branch 9.1 https://github.com/doculibre/constellio.git source

# ---------- Package ---------- #
FROM solr:5.5
COPY --from=source --chown=solr:solr /source/solrHome5/ /opt/solr/server/solr/
