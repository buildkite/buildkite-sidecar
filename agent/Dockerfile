FROM buildkite/agent:3

FROM scratch
COPY --from=0 /buildkite /buildkite
COPY --from=0 /usr/local/bin/buildkite-agent /buildkite/bin/
COPY hooks /buildkite/hooks

FROM busybox:musl
COPY --from=1 /buildkite /buildkite
VOLUME /buildkite