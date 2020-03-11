FROM buildkite/agent:3

FROM scratch
COPY --from=0 /buildkite /buildkite
COPY --from=0 /usr/local/bin/buildkite-agent /bin/busybox /buildkite/bin/
COPY hooks /buildkite/hooks

FROM busybox:musl
COPY --from=1 /buildkite /buildkite
COPY bin/bash /bin/bash
VOLUME /buildkite