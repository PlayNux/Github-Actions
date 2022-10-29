ARG PLAYNUX_CODENAME=unstable
FROM playnux/docker:${PLAYNUX_CODENAME}

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get -qq update && apt-get install -qq meson git python3-git libxml2-utils appstream policykit-1 sudo

RUN groupadd -r playnux && useradd --no-log-init -r -g playnux playnux

COPY entrypoint.sh /entrypoint.sh
COPY check-diff.py /check-diff.py

ENTRYPOINT ["/entrypoint.sh"]
