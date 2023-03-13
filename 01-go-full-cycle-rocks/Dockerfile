FROM golang:1.20 AS builder
WORKDIR /usr/src/app
COPY full-cycle-rocks.go .
RUN go build -ldflags "-s -w" full-cycle-rocks.go


FROM scratch
COPY --from=builder /usr/src/app/full-cycle-rocks full-cycle-rocks
CMD ["./full-cycle-rocks"]