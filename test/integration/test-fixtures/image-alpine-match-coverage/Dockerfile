FROM cgr.dev/chainguard/go:latest@sha256:fa81487f6395a6fd69d9b4f424683f1f690b9ab55cf2603ed597b0415beafdb9 as builder

RUN go install github.com/google/ko@v0.15.1

FROM scratch
COPY . .
COPY --from=builder /root/go/bin/ko /ko
