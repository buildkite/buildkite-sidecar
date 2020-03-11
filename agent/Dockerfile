FROM buildkite/agent:3

FROM scratch
COPY --from=0 /buildkite /buildkite
COPY --from=0 /usr/local/bin/buildkite-agent /bin/busybox /buildkite/bin/
COPY hooks /buildkite/hooks

FROM busybox:musl
COPY --from=1 /buildkite /buildkite
RUN ln -s /bin/sh /bin/bash
VOLUME /buildkite