FROM cgr.dev/chainguard/go@sha256:a4f6cf8c738e90644da3e43cee29865ea8968399e79f696d4bc162a1c4379739@sha256:a4f6cf8c738e90644da3e43cee29865ea8968399e79f696d4bc162a1c4379739 AS builder

RUN go install github.com/google/ko@v0.15.1

FROM scratch
COPY . .
COPY --from=builder /root/go/bin/ko /ko
