FROM buildkite/agent:3

FROM scratch
COPY --from=0 /buildkite /buildkite
COPY --from=0 /usr/local/bin/buildkite-agent /bin/busybox /buildkite/bin/

FROM scratch
COPY --from=1 /buildkite /buildkite
VOLUME /buildkite