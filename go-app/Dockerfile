FROM golang:1.20.6-bookworm AS build

WORKDIR /go-app

COPY go.mod ./
COPY go.sum ./

RUN go mod download && go mod verify

COPY main.go .

# https://github.com/golang/go/issues/58550#issuecomment-1432188779
RUN CGO_ENABLED=0 go build -o /myapp main.go

FROM gcr.io/distroless/base-debian11

COPY --from=build /myapp /myapp
COPY /static /static

EXPOSE 9000

ENTRYPOINT ["./myapp"]