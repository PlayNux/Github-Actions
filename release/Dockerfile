FROM debian:buster-slim

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y xmlstarlet curl git devscripts

# create and use an playnux user instead of root
RUN groupadd -r playnux && useradd --no-log-init -r -g playnux playnux

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
